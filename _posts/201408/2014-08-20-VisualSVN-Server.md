---
layout: post
title: VisualSVN Server 学习
description: 关于对 VisualSVN Server 软件的学习及使用
categories:
- Tool
tags:
- Study
---

## VisualSVN Server 学习笔记

###__安装过程__
1. 打开安装文件

	![Install_1][Install_1]

    可知: 
    + 安装的 VisualSVN Server 的版本为2.7.7
	+ 其中包含的 Apache Http Server 版本号为 2.2.27.
    + 其中包含的 Apache Subversion 版本号为 1.8.9

2. 安装组件选项

	![Install_2][Install_2]
    
    可知: 安装组件有 2 个选项分别为:
    + 同时安装 VisualSVN Server 以及 管理端软件
    + 只安装管理端软件(VisualSVN Server 已经安装在别的机器上)

    勾选项实际是将 svn.exe, svnadmin.exe等文件加入到系统 PATH 中, 设置后在控制台或是其他程序调用时就无需输入以上文件的全路径即可访问到这些文件.
    
3.	安装版本设置

	![Install_3][Install_3]
    
    可知: 
    * 安装时可选择安装标准版(Standard Edition 免费)
	* 或者企业版(Enterprise Edition 付费).
	* 标准版与企业版的不同之处可以点击 Compare Editions…按钮查看比较详情.

4. 安装目录及代码库存放位置

	![Install_4][Install_4]
    
    可知: 
    * 在 Location 后可选择将 VisualSVN Server 安装到具体位置, 点选 Browse… 可打开系统资源管理器界面帮助我们定位到具体目录.
	* 在 Repositories 后可选择将 代码仓库 存放在具体位置, 同样点选 Browse… 可定位具体目录位置.
	* Server Port 表示开启的 Http Server 服务监听的端口号, 当我们选择一个端口号被占用时, 可以在这里进行修改. 如果希望在网络传输中得到更安全的保障可以选择通过https(而不是 http)来传输加密后的数据包.

5. 安装完成

	![Install_5][Install_5]
    
    可知:	勾选 Start VisualSVN Server Manager 以开启 Apache Http Server 服务.



###__使用__



1. 开启界面 

	![Server_1][Server_1]
    
    可知: 	
    * 首先在第一栏我们可以知道当前服务运行的状态
	* 在第二栏我们可以得知日志的记录状态并设置它
	* 在第三栏得知 用户/组 的统计信息, 并且可以对其进行创建.
	* 在第四栏得知代码库的统计信息, 并可以创建或导入.
	* 在右边的树形框中我们可以对代码库, 用户, 组信息展开查看详细的信息, 并对它们进行创建, 修改, 删除操作.

2. 代码库右键菜单

	![Server_2][Server_2]
    
    可知: 通过对代码库选项点击左键弹出的选项栏中
	* 创建代码库
	* 在浏览器中显示代码库的组织结构
	* 对界面右边的现实方案进行设置
	* 导出所有代码库的名称于文件中(默认 txt).

3. 创建代码库

	![Server_3][Server_3]
    
    可知:	在 Repository Name 中填入你想创建的代码库名称.
    
4. 代码库初始情况设置

	![Server_4][Server_4]
    
	可知:	对代码库进行初始情况的设置包含两个选项:
	* 创建空的代码库
	* 创建已经具有文件结构(带有 trunk, branches, tags 三个文件夹)的代码库.

5. 设置代码库初始权限

	![Server_5][Server_5]
    
    可知: 初始权限设置时有三个选项可供用户选择:
	* 任何人不具有读写权限
	* 所有注册用户均可以对该代码库进行读写操作
	* 依照实际需求自定义设置每个用户或群组的权限

6. 代码库生成成功

	![Server_6][Server_6]
    
    可知: 
    * 第一个项目为当前创建的代码库名称
	* 第二个项目为当前创建的代码库地址, 如事例中创建的代码库地址为 https://li_xd/svn/li_ 这个代码组织的结构为:
		https:// 是我们在安装 SVN 时所勾选的 https 服务得出的, 如若不勾选则这里为 http://.
		li_xd 为我的机器的计算机名称, 这里使用计算机名称可以在本局域网中利用系统API而定位到所提供服务的机器.这里可以替换为提供服务机器的IP地址, 而本机访问亦可使用 localhost 进行访问.
	* 第三个项目为当前代码库的访问权限.

7. 代码库创建完成

	![Server_7][Server_7]
    
    可知: 选中该代码库后可以在右边看到代码库中文件的组织形式.
	右键菜单中包含的重要选项有:
	* 将代码库的地址复制到剪切板中
	* 在浏览器中显示文件组织结构
	* 设置用户访问的权限
	* 对该代码库进行重命名

8. 用户右键菜单

	![Server_8][Server_8]
    
    可知: 该菜单中包含三个重要选项
	* 创建新用户
	* 对界面右边的显示方案进行设置
 	* 导出用户名列表于文件中(默认为 TXT)

9. 创建新用户

	![Server_9][Server_9]
    
    可知: 
    * 在第一个选项框中输入账号
	* 在第二个选项框中输入密码
	* 在第三个选项框中重复输入刚才输入的密码.

10. 群组右键菜单

	![Server_10][Server_10]
    
    可知: 该菜单包含三个重要选项
	* 创建新群组
	* 对界面右边的显示方案进行设置
	* 导出群组列表于文件中(默认为 TXT)

11. 创建新群组

	![Server_11][Server_11]
    
    可知: 
    * 第一行可输入群组名称
	* 点选 Add 按钮弹出 Choose User Or Group 列表
	* 点选需要添加到该群组的用户及群组
	* 点击OK按钮成功添加用户/群组于该群组.


[Install_1]:/image/20140820/Install_1.png
[Install_2]:/image/20140820/Install_2.png
[Install_3]:/image/20140820/Install_3.png
[Install_4]:/image/20140820/Install_4.png
[Install_5]:/image/20140820/Install_5.png
[Server_1]:/image/20140820/Server_1.png
[Server_2]:/image/20140820/Server_2.png
[Server_3]:/image/20140820/Server_3.png
[Server_4]:/image/20140820/Server_4.png
[Server_5]:/image/20140820/Server_5.png
[Server_6]:/image/20140820/Server_6.png
[Server_7]:/image/20140820/Server_7.png
[Server_8]:/image/20140820/Server_8.png
[Server_9]:/image/20140820/Server_9.png
[Server_10]:/image/20140820/Server_10.png
[Server_11]:/image/20140820/Server_11.png