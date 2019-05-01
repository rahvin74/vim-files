# vim-files
This is basically just my .vimrc that I use generally.

## Using Vim/Neovim on WSL
In addition to following this tutorial on how to get Terminator working with Windows Subsystem for Linux there are a couple of gotchas/additional steps I had to run.

https://blog.ropnop.com/configuring-a-pretty-and-usable-terminal-emulator-for-wsl/

1. I needed to add the following to my .profile or .bashrc file.
   `export "LIBGL_ALWAYS_INDIRECT=1"`
2. I was having a dBus issue launching. Buried in the comments of the above link I found this this gem:
   `> sudo apt-get install dbus-x11`
   `> sudo /etc/init.d/dbus restart`

The source for that is here: https://github.com/Microsoft/WSL/issues/2016

3. I think I might add DISPLAY=:0 to my .profile or .bashrc file.
4. Lastly, some of the dir colors for the WSL were horrible. Turns out this isn't a WSL thing, just a Linux thing for showing directory permissions. Regardless, it's hideous so I want to change it. Here are some reasources I found for this.

https://github.com/Microsoft/vscode/issues/7556
https://unix.stackexchange.com/questions/241726/fix-ls-colors-for-directories-with-777-permission
https://unix.stackexchange.com/questions/94498/what-causes-this-green-background-in-ls-output
