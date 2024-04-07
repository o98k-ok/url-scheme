# url-scheme
URL Scheme collections for MacOS


## 介绍

URL Scheme是应用快捷操作的一种解决方案。
由于不同应用支持的情况一言难尽， 所以在这里总结下工作中比较常用的URL Scheme。

仅限 **MacOS** 端，想了解更多内容可以查看：[URL Scheme收集](https://gist.github.com/JamesHopbourn/046bc341e7debfd0c86e3b388d983c53)


## vscode

### 1. 方案

安装插件：
* [vscode-commands-executor](https://github.com/mihai-vlc/vscode-commands-executor): Enables the execution of vscode commands on open startup vscode via the vscode:// URI

### 2. 样例

* 快速打开插件市场
```shell
open 'vscode://ionutvmi.vscode-commands-executor/runCommands?data=[{"id": "workbench.extensions.action.installExtensions"}]'
```

* 打开主题配色方案
```shell
open "vscode://ionutvmi.vscode-commands-executor/runCommands?data=[{\"id\": \"workbench.action.selectTheme\"}]"
```

* 关闭其他标签页
```shell
open "vscode://ionutvmi.vscode-commands-executor/runCommands?data=[{\"id\": \"workbench.action.closeEditorsToTheRight\"}]"
```
### 3. 扩展

* 可以结合Alfred做更多事情，参考这里[vscode-flow](https://github.com/o98k-ok/vscode-remote-flow)
* vscode command line 也很好用
* 如何寻找命令ID？
	1. 使用command line 找到命令
	2. 点击进行设置
	3. 双击选择Copy Command ID

## obsidian

### 1. 方案

安装插件：
* [obsidian-advanced-uri](https://github.com/Vinzent03/obsidian-advanced-uri): allows you to control many different features in Obsidian just by opening some URIs.

### 2. 样例

* 启动全局搜索
```shell
open 'obsidian://advanced-uri?vault=obsidian&commandid=global-search%253Aopen'
```
* 启动quickapp
```shell
open 'obsidian://advanced-uri?vault=obsidian&commandid=quickadd%253ArunQuickAdd'
```
### 3. 扩展

* 可以结合Alfred做更多事情，参考这里[vscode-flow](https://github.com/o98k-ok/vscode-remote-flow)
* obsidian 本身也有command line入口，功能类似
* 如何寻找命令的ID？
	1. 调出command line
	2. Advanced URI: copy URI for command

## 飞书

飞书是工作中常用的IM软件，支持一些URL Scheme方案：[lark](https://open.feishu.cn/document/common-capabilities/applink-protocol/applink-introduction/applink-structure)

### 1. 样例

* 快速找到聊天对象
```shell
open "lark://applink.feishu.cn/client/chat/open?openId=${openID}"
```
* 打开工作台
```shell
open "lark://applink.feishu.cn/client/workplace/open"
```
* 打开日历
```shell
open "lark://applink.feishu.cn/client/calendar/open"
```

### 2. 扩展
* lark、feishu作为scheme取代https都是可以的
* 样例一中的openID需要调用接口获取
