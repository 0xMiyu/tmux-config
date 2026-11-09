My Tmux Config Stuff
====================

## First, download Tmux Package Manager from Github

```sh
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

## Next, make sure fish is your default shell and run killall tmux

## If it doesn't work, run tmux set-option -g default-shell /opt/homebrew/bin/fish

## Install the plugins

Start tmux, then press prefix + I (`Ctrl-Space`, then `Shift-i`).

## Moving from an older version of this config

Older versions used `rose-pine/tmux`, which installs to the same folder as `catppuccin/tmux` (`plugins/tmux`).
TPM skips a plugin if its folder already exists, so delete the old one before installing:

```sh
git -C ~/.config/tmux/plugins/tmux remote get-url origin   # check that it shows rose-pine
rm -rf ~/.config/tmux/plugins/tmux
```

Then press prefix + I and restart tmux with `tmux kill-server`. This closes all sessions.
