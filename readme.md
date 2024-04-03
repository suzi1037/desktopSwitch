# Explanation

Originated from  https://github.com/pmb6tz/windows-desktop-switcher

# Changes from original version:

The code has been simplified, retaining only the core switching functionality.

* Use Win+Number keys to switch desktops.
* Other functionalities, such as creating and deleting desktops, have been removed.
* The most important change is the modification of the logic to avoid the bug of cycling activation of Win+Tab, such as
  1->3 or 3->1:

![bug.gif](bug.gif)

# Usage

1. Install AutoHotkey 1.1
2. Run `desktopSwitcher.ahk`
3. Use Win+Number keys to switch desktops.

# Increasing the Number of Desktops

By default, it supports 3 desktops. To support more desktops, you can modify desktopSwitcher.ahk as follows:

```text
DesktopCount = 4                     ; Change it to 4
...
#3::switchDesktopByNumber(3)
#4::switchDesktopByNumber(4)         ; Add this line
```

# as i know

it is not perfect, but it works for me.