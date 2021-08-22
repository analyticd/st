# st - simple terminal

st is a simple terminal emulator for X which sucks less.

Update: This repo builds on macOS Catalina as long as you install the
dependencies.

![Screenshot](https://imgur.com/a/jGLo7W4 "Suckless Terminal on macOS Catalina")

# Requirements

In order to build st you need the Xlib header files.

Update: if you are building on macOS these can be obtained from macports.
Note: I suggest you not use XQuartz but instead the version MacPorts provides
as it is newer and does faster output rendering.

# Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

```sh
make clean install
```
Note: If you are building on macOS you may likely be using Brew and possibly
also MacPorts for some things. Note that brew doesn't like you to change
permissions on /usr/local/ so you can, as you see above, just install without
sudo.

# Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

```sh
tic -sx st.info
```

See the man page for additional details.

# Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
