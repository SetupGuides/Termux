# Termux

Termux is an Android terminal emulator and a linux environment. It can be used to run most
Linux software without root. This guide will help at setting up and configuring Termux.

## Installation

1. Download [Termux](https://termux.com/). (Installing `Termux-API` is also recommended.)
2. Update packages. `$ apt update && apt upgrade`[^1]
3. Install Termux API. `$ apt install termux-api`[^1]
4. Configure access to external storage. `$ termux-setup-storage`[^2]

## Recommended Customizations

- [zsh](https://github.com/SetupGuides/ZSH)
- [Neovim](https://github.com/SetupGuides/Neovim)

## Enabling SSH Remote Connection

Termux supports remote connections via the Secure SHell (SSH) protocol. Follow the instructions below to install and configure SSH.

1. Install SSH. `$ apt install openssh`
2. Add `sshd -p <port>`[^3] to your `.zshrc` (Or `.bashrc`, if you are not using zsh) file.
3. Set SSH password. `$ passwd` (This will prompt you to enter a password twice.)
4. Reload your terminal or manually run the command `sshd -p <port>`.
5. Using another machine, connect to Termux using `$ ssh <user>@<ip> -p <port>`

[^1]: If you encounter an error, run `$ termux-change-repo` to use a mirror and try again.
[^2]: Android might prompt you to allow access to external storage. Press "*Allow*" to continue.
[^3]: The SSH port is usually 22. However, if you are using a non-rooted Android device, use `8022` or any port above 1024.

