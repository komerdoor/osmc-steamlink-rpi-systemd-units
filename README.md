# Steamlink systemd units for Steamlink on Raspberry Pi (OSMC)

# Installation

- Add a user called `steamlink` using `useradd steamlink`
- Add `steamlink` user to required groups using `usermod -a -G audio,video steamlink`
- Install steamlink into home directory of `steamlink` user following the instructions at:

https://steamcommunity.com/app/353380/discussions/0/1743353164093954254/

- Copy the systemd unit files to `/etc/systemd/system`
- Run `systemctl daemon-reload`

# Switch to Steamlink

Run `systemctl start steamlink`

# Switch to Kodi

Run `systemctl start mediacenter`
