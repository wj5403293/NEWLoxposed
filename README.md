[下载最新版](http://jkx.dotcog.nhely.hu/d/loxposed.apk)

# Loxposed - 免Root Xposed框架

Loxposed是一个基于LSPosed核心的免Root Xposed框架，通过修改软件的安装包实现Xposed注入。

## 主要优点

- 支持Modern Xposed API（LSPosed API 100）, New XSharedPreferences, Remote Preferences（暂不支持监听数据变化）, Remote Files。
- 对比LSPatch，该框架性能更好，软件的启动速度更快，内存占用也更少。

## 使用方法

1. **修改文件夹名（可选）**  
   - 修改Loxposed安装包中的`assets/loxdir.txt`，替换成自己喜欢的文件名。这个文件名会作为SD卡下放置注入软件修改后的安装包以及储存注入软件原始签名和New XSharedPreferences数据的文件夹名，然后安装。  
   - 默认文件名为`Loxposed`。

2. **授予文件访问权限**  
   - 先给予该框架所有文件访问权限，打开框架会自动跳转到所有文件访问权限的设置界面，然后给予该权限。

3. **修补目标软件**  
   - 在任意文件管理器中找到目标软件的APK，选择打开方式为Loxposed框架。
   - 等待修补完成，完成后在SD卡下找到以自己设置的文件名命名的文件夹，其中的`patched.apk`就是修改过的安装包。
   - 直接安装`patched.apk`，安装后需给予目标软件所有文件访问权限。

4. **启用模块**  
   - 打开框架，开启要使用的模块右上角的开关。
   - 长按模块，点击“模块作用域”，勾选目标软件即可。

5. **特殊模块激活（如SimpleHookL和WebViewPP）**  
   - 将模块APK用上述步骤修改后安装。
   - 在框架中开启该模块，并给予该模块所有文件访问权限即可激活使用。

6. **刷新加载器和模块信息**
   - 每次该框架被安装（比如第一次安装或更新）后都要在打开框架并点击右上角的菜单去刷新加载器，每次有模块被安装都要刷新模块信息或重新打开该框架。