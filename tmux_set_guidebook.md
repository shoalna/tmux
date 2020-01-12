## Summary some useful setting about TMUX

#### 1. get conf file

​	vim ~/.tmux.conf

 	~: (チルダ)means user's home-directory, if we cd ~ , we will get to home



#### 2. set it

```bash

# Send prefix
# I perfer bind C-a, just follow your heart

set-option -g prefix C-a

unbind-key C-a

bind-key C-a send-prefix

# Use Alt-arrow keys to switch panes

bind -n M-Left select-pane -L

bind -n M-Right select-pane -R

bind -n M-Up select-pane -U

bind -n M-Down select-pane -D

# Shift arrow to switch windows

bind -n S-Left previous-window

bind -n S-Right next-window

# Mouse mode
# prefix + q to turn mouse-mode on and w to off
# When turn mouse mode on, cannot use copy-paste by mouse right-click
# So turn mouse-mode off to activate copy-paste
# If mouse-mode is off, you can only slide up-and-down by prefix+[
# When mouse-mode is on, just use Scroll wheel

bind q set -g mouse on\; display-message "mouse mode on"

bind w set -g mouse off\; display-message "mouse mode off"

# Set easier window split keys

bind-key v split-window -h

bind-key h split-window -v


# Easy config reload

bind-key r source-file ~/.tmux.conf \; display-message "tmux.conf reloaded"
```

