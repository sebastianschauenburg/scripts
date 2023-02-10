# sudo X

sudox is a small wrapper for sudo to "easily" enable X11 forwarding when switching to another user via sudo **remotely**. 

Basically this sets the `MIT-MAGIC-COOKIE` in the `.Xauthority` file and also sets the `XAUTHORITY` environment variable, without enabling running X11 applications to all users (e.g. disabling authentication with `xhost`).


# use case

You log in to a server with your own account and need to run a GUI application. For example: some applications require running a GUI for setup or maintenance.


# future

I don't expect do to much maintenance work on this project or extend it a lot. It is built to scratch a very specific itch (use case) and it solves that (works for me).
