# WebStorm 常用技巧笔记

WebStorm 是 mac 下的精品 IDE，有很多 Visual Studio 不具备的亮点。  
本文收集一些使用技巧、快捷键和答疑。

调整 Layout 以突出编码区域，更适合笔记本和16:9显示器：
- [Preferences] Appearance & Behavior > Appearance：勾选 Widescreen ... layout
- [Menu] View: 把 Toolbar, Tool Buttons, Status Bar, Navigation bar 全关掉

允许解析 module 等 node 全局变量：
- [Preferences] Languages & Frameworks > JavaScript > Libraries: 勾选 Node.js Globals

隐藏代码折叠的箭头：
- [Preferences] Editor > Code Folding: 取消 Show code folding outline

在方法之间显示横线：  
  ![image](https://cloud.githubusercontent.com/assets/1503156/6655574/4a045f08-cb3e-11e4-8572-cf07591dc102.png)
- [Preferences] Editor > General > Appearance: 勾选 Show method separators

从项目中排除第三方文件，优化代码搜索结果：
- [Preferences] Project > Directories: 选中不需要的文件夹，点上面的 Excluded，例如这样设置：  
![image](https://cloud.githubusercontent.com/assets/1503156/6655584/c4e5bf5a-cb3e-11e4-92ae-73f546066565.png)  
也可以在 [Project] 面板上的文件夹点击右键，选择 Mark Directory As > Excluded

不在 [Project] 显示已排除的第三方文件：
- [Project] 点击 "Scope按钮"，选择 Project Files  
![image](https://cloud.githubusercontent.com/assets/1503156/6655587/eb5a3ef4-cb3e-11e4-8f56-4ec71755fa2c.png)

按文件类型排序：
- [Project] 点击齿轮下拉菜单，选中 Sort by Type 和 Folders Always on Top
![image](https://cloud.githubusercontent.com/assets/1503156/6655599/3ff51f9c-cb3f-11e4-8973-a52bbb223cc1.png)

在 [Project] 中定位到当前编辑的脚本：
- 点击图中的小图标  
![image](https://cloud.githubusercontent.com/assets/1503156/6655611/fdac47d6-cb3f-11e4-83ab-dc79eca5adf5.png)

