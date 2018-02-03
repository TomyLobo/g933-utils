# Yotredash

[![Gitter](https://badges.gitter.im/g933-utils/Lobby.svg)](https://gitter.im/g933-utils/Lobby)

An application to configure and control the Logitech G933 wireless headset

# Usage

You will need the udev rules installed on your system. Copy `90-logitech.rules` to `/etc/udev/rules.d/` and add your user to the `logitech` group, then run these commands:
```
udevadm control --reload-rules
udevadm trigger
```
and log out and back in, or alternatively just reboot.

You can build the tool with Cargo by navigating to the git clone directory and executing `cargo build --release`. The executable will now be in the `target/release` directory.

After building, try running `./target/release/g933-utils --help` to see an overview of the commands.

# Hacking

There is a Wireshark lua script in the `notes` directory that provides better parsing for the HID++ protocol that this and other Logitech devices use.  
Link this script into your `~/.config/wireshark/plugins` directory, and wireshark should load it automatically.

# Support Me

I do a lot of work on this project and others. If you want to support me and my work so I can keep maintaining these projects, please consider becoming a patron: https://patreon.com/ashkitten
