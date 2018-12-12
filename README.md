# Steamlink systemd units for Steamlink on Raspberry Pi (OSMC)

# Installation

1. Add a user called `steamlink` using `useradd steamlink`
2. Add `steamlink` user to required groups using `usermod -a -G audio,video steamlink`
3. Install steamlink into home directory of `steamlink` user following the instructions at:

https://steamcommunity.com/app/353380/discussions/0/1743353164093954254/

4. Copy the systemd unit files to `/etc/systemd/system`
5. Run `systemctl daemon-reload`

*Note:* If you want to install Steamlink inside the `osmc` home directory, skip steps 1 and 2 above and use `osmc` instead of `steamlink` as the user. In the `steamlink.service` unit file, replace `User=steamlink` with `User=osmc`.

# Switch to Steamlink

Run `systemctl start steamlink`

# Switch to Kodi

Run `systemctl start mediacenter`
