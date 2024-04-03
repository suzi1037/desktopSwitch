# 说明

源自 https://github.com/pmb6tz/windows-desktop-switcher

# 变化:

主要是简化了代码，只保留了核心切换功能。

* 使用win+num键切换桌面
* 删除了除切换功能外的其他功能：包括创建，删除桌面
* 对于我，最重要的：修改了逻辑，避免循环激活win+tab的bug，比如1->3或者3->1时:

![bug.gif](bug.gif)

# 使用方法

1. 安装autohotkey 1.1
2. 运行`desktopSwitcher.ahk`
3. 使用win+num键切换桌面

# 增加桌面数量

默认支持3个桌面，要支持更多桌面，可以修改`desktopSwitcher.ahk`，如下：

```text
DesktopCount = 4        ; 修改成4
...
#3::switchDesktopByNumber(3)
#4::switchDesktopByNumber(4)         ; 增加这一行
```