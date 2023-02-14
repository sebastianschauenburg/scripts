# sudo X

sudox is a **small wrapper** for `sudo` to "easily" facilitate X11 forwarding, when switching to another user via sudo **remotely**. 

Basically this sets the `MIT-MAGIC-COOKIE` in the `.Xauthority` file and also sets the `XAUTHORITY` environment variable. By using this, you do not have to disable authentication (with `xhost`) globally (e.g. decreasing security).


# use case

You log in to a server with your own account and need to run a GUI application as another user. For example: some applications require running a GUI for setup or maintenance.


# example

Use `sudox` instead of `sudo` with your usual options and arguments. Example:

```
user@host:~$ sudox -i -u daemon
[sudo] password for user:
daemon@host:~$ xterm
```


# future

I don't expect do to much maintenance work on this project or extend it a lot. It is built to scratch a very specific itch (use case) and it solves that (works for me).
