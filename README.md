SublimePaneNavigation
============================

In Sublime Text 3, when you have multiple panes open within a single window, holding down `ctrl+pageup` will cycle through *all* open tabs in all panes.

That's lame. It should only cycle through the tabs open in the currently active pane.

## Installation
* Install [Package Control](https://sublime.wbond.net/installation)
* Open the Command Palette (`ctrl+shift+p`, or find it in the "Tools" menu)
and select "Package Control: Install Package"
* Select "PaneNavigation" from the installation panel

## Usage
`ctrl+tab` and `ctrl+shift+tab` have been remapped to cycle through the tabs within the active pane.

## Other Notes
To switch which pane is active, use the Sublime's builtin `"focus_neighboring_group"` command and keybinds:
```
    { "keys": ["ctrl+k", "ctrl+left"], "command": "focus_neighboring_group", "args": {"forward": false} },
    { "keys": ["ctrl+k", "ctrl+right"], "command": "focus_neighboring_group" },
```

To move tabs between panes, use Sublime's builtin `"move_to_neighboring_group"` command and keybinds:
```
    { "keys": ["ctrl+k", "ctrl+shift+left"], "command": "move_to_neighboring_group", "args": {"forward": false} },
    { "keys": ["ctrl+k", "ctrl+shift+right"], "command": "move_to_neighboring_group" },
```

(These keybinds are already built into Sublime by default)

##Acknowledgements
This code was basically copied wholesale from Boris Treskunov's [Pane Navigation](https://github.com/borist/SublimePaneNavigation) plugin; all credit goes to him, the original author.

His plugin was only set to work in Sublime Text 2 and it seems to be abandoned, so I created this plugin to bring it to Sublime Text 3.

Boris, if you're reading this and you'd like me to take this down or transfer control to you, let me know.