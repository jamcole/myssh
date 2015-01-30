## About

**myssh** wraps ssh connections to override the remote ~/.profile and ~/.bashrc files with your local *~/.mysshrc* using netcat locally and  netcat, telnet, or bash's /dev/tcp/ functionality on the remote host

**myssh** was inspired by [sshrc](https://github.com/Russell91/sshrc) and was created as a one-off when I couldn't remember the name of the sshrc project :-D

sshrc is more mature, uses xxd instead of netcat and port forwarding, you probably should use it instead

## Usage

* **myssh** [additional SSH options] user@host

## Requirements

* Local: ssh, bash, netcat
* Remote: sshd, bash, One of the following: netcat, telnet & sed, bash's /dev/tcp/ functionality

## Installation

1. Checkout the **myssh** project or download the **myssh** file
2. Make **myssh** executable
3. Create a *~/.mysshrc* file with the rc settings you'd like (mysshrc.example is a good start)

## Special Thanks

Thanks to [sshrc](https://github.com/Russell91/sshrc) for the concept

## Warnings / Known Issues

* If the 12345 port is already in use, myssh will not connect; this is on purpose, you don't want to grab another user's .mysshrc file.  In the future we should drop the remote forwarded port after the file copy.
* **myssh** will trade your first-born for a frapuccino and will kick your dog, you have been warned!
