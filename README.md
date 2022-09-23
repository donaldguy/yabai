# fyabai

Personal patches for yabai. Cherry-pick them to your own fork if you want to use them:

- Revert removal of window borders
- Upgrade IPC from unix sockets to mach messages
- Window borders are drawn half inside and half outside the window to avoid gaps
- Animation fade for smoother animations
- Allow only one child at a time to zoom to parent node
- Zoomed windows occlude windows below in the next-window-in-direction calculation
- Focus closest window on application termination
- Focus sibling window node on window destruction
- Auto Padding for ultrawide displays, only applies to displays with aspect
ratio greater than `auto_padding_min_aspect` and tries to achieve a width of
`auto_padding_width` and a height of `auto_padding_height` for any window
(except when there is only one window, then it will try to make the window 2*auto_padding_width).
Fullscreen zoom will make the window zoom to use the full screen area. These are the defaults:
```bash
yabai -m config auto_padding off
yabai -m config auto_padding_min_aspect 2.33
yabai -m config auto_padding_width 840
yabai -m config auto_padding_height 1200
```
