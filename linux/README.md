# Linux Commands Directory

## 5 commands to check memory usage on Linux
Ref: [Resource](https://www.binarytides.com/linux-command-check-memory-usage/) 
```
$ free -m
$ cat /proc/meminfo
$ vmstat -s
$ top
$ htop
```

## How To Use Linux Screen for background task running
Ref: [Resource](https://linuxize.com/post/how-to-use-linux-screen/)

The screen package is pre-installed on most Linux distros nowadays. You can check if it is installed on your system by typing:
```
screen --version
```
If you don’t have screen installed on your system, you can easily install it using the package manager of your distro.
Install Linux Screen on Ubuntu and Debian:
```
sudo apt update
sudo apt install screen
```
### Detach from Linux Screen Session
You can detach from the screen session at any time by typing:
```
Ctrl+a d
```
The program running in the screen session will continue to run after you detach from the session.

### Reattach to a Linux Screen
To resume your screen session use the following command:
```
screen -r
```
In case you have multiple screen sessions running on your machine, you will need to append the screen session ID after the `r`switch.

To find the session ID list the current running screen sessions with:
```
screen -ls
```
