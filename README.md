# revolver

## basic work

crete a vars:
1. Shoots = [];
2. last_system_clipboard_value = string;
3. is_revolver_mode = false;

add listener on !#s shortcut
on !#s reads current clipboard value and assign it to `last_system_clipboard_value` var
	is_revolver_mode = true
	if is_revolver_mode === true
		on ^c wait 50ms, read clipboard value, add it to Shoots, write clipboard value on Shoots[0]
		on ^v paste previously writed to clipboard Shoots[0], remove first value from Shoots, write to lcipboard value of Shoots[0]
	if is_revolver_mode === false
		write last_system_clipboard_value to system clipboard


## iterface

on !#c holding shows your Shoots array at left part of screen. Pointer events none and on any click this window will disappear

when you in revolver mode at tray you'll see the revolver clip icon


## libs

[clipboard lib](https://github.com/golang-design/clipboard)
