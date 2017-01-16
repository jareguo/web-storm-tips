# WebStorm 常用技巧笔记
[(Edit This Page)](https://github.com/jareguo/web-storm-tips/edit/master/README.md)

## 通用技巧

- 几乎在所有面板包括弹出窗口里，都能直接键入名字进行快速跳转。例如
    - 在查找结果中增量查找
    - 在 Outline 窗口中快速跳转
    - 在 Project、Recent File 中快速跳转

## 常用快捷键(Mac)：

导航：
- **打开文件**：`Shift + ⌘ + O` (被我改成了和 Chrome 相同的 `⌘ + O`)
    - 文件名前面或后面加上`/`可打开目录
- 打开符号：`Alt + ⌘ + O`
- 搜索任意：双击 `Shift`
- 跳转到声明：`⌘ + Alt + B`
- 跳转到实现：`⌘ + B`
- 搜索所有引用：我定义的是 `Shift + F12`
- **弹出文件结构列表**(Outline)：`⌘ + F12`
- 弹出最近关闭的文件列表(Recent File)：`⌘ + E`
    - 之后直接键入文件名可快速跳转到最近关闭的文件，找不到的话按回车则在项目中查找。
- 跳转到下一查找结果：`Alt + ⌘ + Down`
- 弹出外部资源菜单：(在 Tab 标签上) `⌘ + Click`
- 添加书签：`F3`，浏览书签：`⌘ + F3`
- 跳转到代码块开头：`Alt + ⌘ + [`
- 在左右（花）括号之间跳转：`Ctrl + M`

视图：
- 跳转回编辑面板: `Esc`
- 切换下一个代码标签：`Ctrl + Tab` 或 `Shift + ⌘ + ]`
- 切换上一个代码标签：`Shift + ⌘ + [`
- 最大化/还原编辑面板：双击标签栏
- 显示所有视图边栏：显示双击并按住 `⌘`
- 关闭当前显示查找结果标签页：`Ctrl + Shift + F4`

编辑：
- 插入代码片段(Code Snippet)：`⌘ + J`
- 重构：`Ctrl + T`
- 重命名（变量等）：`Shift + F6`
- 重构预览时，从搜索结果中排除：`Delete`
- 格式化代码：`Alt + ⌘ + L`
- 缩进对齐：`Ctrl + Alt + I`
- **弹出 Intention Actions**: `Alt + Enter`
- 同时选中下一个相同代码块：`Ctrl + G`
- 同时选中所有相同代码块：`Ctrl + ⌘ + G`
- 一些 Unix 终端快捷键：`Ctrl + A/E/K`

行操作：
- 复制(选中)行：`⌘ + D`
- **上移(选中)行**：`Shift + Alt + Up`
- 上移(选中)语句：`Shift + ⌘ + Up`
- 在上面插入新行：`Alt + ⌘ + Enter`
- 在下面插入新行： `Shift + Enter`
- 删除行：`⌘ + Delete`

显示：
- 显示方法参数说明：`⌘ + P`
- 显示光标处的代码文档：`F1`
- 快速查看定义：`Alt + Space`
- 高亮当前文件中所有选中字段：`Shift + ⌘ + F7` (然后`⌘ + G`跳转下一个)
- 扩大选中的代码块：`Alt + Up`（可以用来选词，按越多次选中的代码块范围越大）
- 折叠/展开代码块：`⌘ + -/=`
- 光标向上/向下移动同时滚动视图(Move Up)：我定义的是 `Shift + ⌘ + I/K`

其它：
- 激活搜索框 "Match Case": `Alt + C`
- 激活搜索框 "Words": `Alt + R`
- 重复最近的搜索：焦点在输入框时按 `Down`
- 新建草稿文件: `⌘ + Shift + N`

## 调整 Layout 以突出编码区域，更适合宽屏：
- [Preferences] Appearance & Behavior > Appearance：勾选 Widescreen ... layout
- [Menu] View: 把 Toolbar, Tool Buttons, Status Bar, Navigation bar 全关掉

## 允许解析 module 等 node 全局变量：
- [Preferences] Languages & Frameworks > JavaScript > Libraries: 勾选 Node.js Globals

## 隐藏代码折叠的箭头：
- [Preferences] Editor > Code Folding: 取消 Show code folding outline

## 从项目中排除第三方文件，优化代码搜索结果：
- [Preferences] Project > Directories: 选中不需要的文件夹，点上面的 Excluded，例如这样设置：  
![image](https://cloud.githubusercontent.com/assets/1503156/6655584/c4e5bf5a-cb3e-11e4-92ae-73f546066565.png)  
也可以在 [Project] 面板上的文件夹点击右键，选择 Mark Directory As > Excluded

## 不在 [Project] 显示已排除的第三方文件：
- [Project] 点击 "Scope按钮"，选择 Project Files  
![image](https://cloud.githubusercontent.com/assets/1503156/6655587/eb5a3ef4-cb3e-11e4-8f56-4ec71755fa2c.png)

## 按文件类型排序：
- [Project] 点击齿轮下拉菜单，选中 Sort by Type 和 Folders Always on Top
![image](https://cloud.githubusercontent.com/assets/1503156/6655599/3ff51f9c-cb3f-11e4-8973-a52bbb223cc1.png)

## 在 [Project] 中定位到当前编辑的脚本：
- 点击图中的小图标  
![image](https://cloud.githubusercontent.com/assets/1503156/6655611/fdac47d6-cb3f-11e4-83ab-dc79eca5adf5.png)

## 去掉 spell checking：
- [Preference] Editor > Inspections: 把 spelling 项的复选去掉

## 屏蔽对象定义时最后多写一个逗号引起的报错：
- [Preference] Editor > Inspections > JavaScript > General: 取消 Last comma in object literal

## 减少 jshint 报错
- 在项目的 `.idea/jsLinters/` 目录下添加 [jshint.xml](https://raw.githubusercontent.com/jareguo/web-storm-tips/master/jshint.xml)

## Postfix Completion
- [Preferences] Editor > General > Postfix Completion：启用你喜欢的选项

## 开启 ES6 支持
- [Preferences] Languages & Frameworks > JavaScript：选择 `ECMAScript 6`  
（需要重启 WebStorm 才能生效）

## 自动识别当前文件的缩进类型
- [Preferences] Editor > Code Style：选择 Detect and use existing file indents for editing

## 滚动条快速滚动到选中位置
- 系统设置中选中该项  
![image](https://cloud.githubusercontent.com/assets/1503156/11030739/f9231abe-870a-11e5-93d2-404510128b17.png)

-----

## 允许输入中文标点

WebStrom 10 开始中文标点无法输入，这是新版 JDK 的 bug，临时解决方法是
 1. 按下 ⌘ + Shift + A
 2. 在弹出框中输入 jdk
 3. 选择 Switch IDE boot JDK，然后会列举当前**未启用的** JDK 版本
 4. 选择 1.8.0_45 或者更低版本的 JDK（如果没有需要自己手动安装到系统中）

最后重启 WebStrom 就能输入中文标点了，不过字体渲染会稍微难看点。要切换回来的话，方法一样，只不过最后换回 builtin 版本的 JDK。

## WebStrom 作为 merge 工具  
`/Applications/WebStorm.app/Contents/MacOS/webstorm merge $(cd $(dirname "$LOCAL") && pwd)/$(basename "$LOCAL") $(cd $(dirname "$REMOTE") && pwd)/$(basename "$REMOTE") $(cd $(dirname "$BASE") && pwd)/$(basename "$BASE") $(cd $(dirname "$MERGED") && pwd)/$(basename "$MERGED")`

## WebStrom 作为 diff 工具  
`/Applications/WebStorm.app/Contents/MacOS/webstorm diff $(cd $(dirname "$LOCAL") && pwd)/$(basename "$LOCAL") $(cd $(dirname "$REMOTE") && pwd)/$(basename "$REMOTE")`
