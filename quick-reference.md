# Kinesis Advantage 2 Programming Quick Reference

## Key
- x+y means hold x and y together. 
- x+y c means press and hold x and y together. Release x and y. Then press c.

## Quick Reference
| What            | Key Combination      | Notes
| -------------   | ------------------   | -------------
| Power User Mode | progm + shift + esc  | Toggle On / Off
| V Drive         | progm + F1           | Mount / Unmount V Drive (Power User Mode must be ON)
| Status Report   | progm + esc          | Types a status report
| Hard Reset      | progm + F9           | Unplug keyboard, press and hold while plugging back in. WARNING: This is not a full factory reset.
| New Layout      | progm + F2 X         | Where X is the hotkey
| Activate Layout | progm + X            | Where X is the hotkey
| Key Clicks      | progm + F8           | Toggle clicking sound on/off
| Macro Speed     | progm + F10 + 3      | Substitute "3" with 1 - 9. The default is three. Nine works well for most uses.


## Power User Mode & Onboard Drive

One can program kinesis keyboard shortcuts in text editor via power user mode. To activate:
`progm + shift + esc` and then `progm + F1`

## Layouts
Layouts are stored in `{#}_{mode}.txt` files in active/ folder in the onboard drive. For example `1_mac.txt` and `2_qwerty.txt` mean the first mac layout and the second qwerty layout.

To active the layout, one needs to activate the mode first and then the layout, for example
1. `progm + F5` and then `progm + 1` to activate `1_mac.txt`
2. `progm + F3` and then `progm + 2` to activate `2_qwerty.txt`
3. `progm + F6` and then `progm + g` to activate `g_pc.txt`

In the layout, keys are mapped from `[src]>[dest]` fashion (or in another word `[from]>[to]`). For example:

```
[caps]>[lctrl]  ==> physical [Caps Lock] key is mapped to [Left Ctrl] key
[up]>[down]     ==> physical [Arrow Up] key is mapped to [Arrow Down] key
...
```

[Some common keys are](https://github.com/KinesisCorporation/Advantage2-SmartSet-App/blob/master/Common/u_const.pas):

### Mac
```
(VK_RETURN, 'ent', 'return')
(VK_RETURN, 'enter', 'return')
(VK_BACK, 'bspc',  'delete')
(VK_BACK, 'bspace',  'delete')
(VK_DELETE, 'del', 'fwd-' + #10 + 'delete'))
(VK_DELETE, 'delete', 'fwd-' + #10 + 'delete'))
(VK_MENU, 'Opt', 'Opt', 'alt'))
(VK_LMENU, 'lalt', 'Left' + #10 + 'Opt', '', '', '', false, false, '', true, False, 0, '', 'Left Option'))
(VK_RMENU, 'ralt', 'Right' + #10 + 'Opt', '', '', '', false, false, '', true, False, 0, '', 'Right Option'))
(VK_LWIN, 'Cmd', 'Cmd', 'lwin'))
(VK_LCMD_MAC, 'lwin', 'Left' + #10 + 'Cmd'))
(VK_RWIN, 'rwin', 'Right' + #10 + 'Cmd'))
```
### FN
```
  ConfigKeys.Add(TKey.Create(VK_F1, 'F1'));
  ConfigKeys.Add(TKey.Create(VK_F2, 'F2'));
  ConfigKeys.Add(TKey.Create(VK_F3, 'F3'));
  ...
  ConfigKeys.Add(TKey.Create(VK_F5, 'F24'));
```

### Control Keys
```

(VK_ESCAPE, 'escape', 'Esc')
(VK_PAUSE, 'pause', 'Pause')
(VK_PRINT, 'prtscr', 'Print')
(VK_SNAPSHOT, 'prtscr', 'Print')
(VK_SCROLL, 'scroll', 'Scroll')
(VK_TAB, 'tab', 'Tab')
(VK_CAPITAL, 'caps', 'Caps')
(VK_SPACE, 'space', 'Space')
(VK_LSPACE, 'lspc', 'Space')
(VK_RSPACE, 'rspc', 'Space')
(VK_INSERT, 'insert', 'Insert')
(VK_HOME, 'home', 'Home')
(VK_END, 'end', 'End')
(VK_NEXT, 'pdown', 'Page')
(VK_PRIOR, 'pup', 'Page')
(VK_RIGHT, 'right', 'right')
(VK_LEFT, 'left', 'left')
(VK_UP, 'up', 'up')
(VK_DOWN, 'down', 'down')
(VK_SHIFT, 'Shift', 'Shift')
(VK_LSHIFT, 'lshift', 'Left')
(VK_RSHIFT, 'rshift', 'Right')
(VK_CONTROL, 'Ctrl', 'Ctrl')
(VK_KP_NUMLCK, 'numlk', 'Num')
(VK_KP_MENU, 'menu', 'PC')
```
