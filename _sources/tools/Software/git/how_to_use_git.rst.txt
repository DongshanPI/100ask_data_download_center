==================
🛠Git简明教程
==================

1. 安装GIT
===========

在Windows下，Git名为msysGit，从 https://gitforwindows.org 上下载安装文件，双击安装即可，安装选项很多，使用默认选项即可。
如果下载慢，可以在百度上搜：Git-2.28.0-64-bit.exe，自行下载。

对于Windows或Linux，它们的命令行用法相似，对于Windows，进入Git命令行的方法是在 ``开始->所有程序->Git`` 下启动 Git Bash。
Git Bash的命令用法跟Linux完全一样，比如cd、ls等命令。

2. GIT常用命令
===============

+-----------+-----------------------+--------------------------------------------------------------------------+
|GIT命令    |说明					|示例                                                                      |
+===========+=======================+==========================================================================+
|clone      |克隆，从远程下载仓库	|git clone https://e.coding.net/weidongshan/01_all_series_quickstart.git   |
+-----------+-----------------------+--------------------------------------------------------------------------+
|pull       |拉取，从远程更新仓库	|git pull origin                                                           |
+-----------+-----------------------+--------------------------------------------------------------------------+
|log        |查看本地仓库的记录		|git log，快捷键：f前翻、b后翻、q退出                                      |
+-----------+-----------------------+--------------------------------------------------------------------------+
|status     |查看本地仓库状态，		|git status                                                                |
|           |比如有无修改，         |                                                                          |
|           |修改有无提交进仓库里	|                                                                          |
+-----------+-----------------------+--------------------------------------------------------------------------+
|tag        |查看标签，或是打标签   |git tag     // 查看标签                                                   |
|           |                       |git tag v2  // 打标签                                                     |
+-----------+-----------------------+--------------------------------------------------------------------------+
|checkout   |提取出某个版本         |使用git log查看版本，可以看到这样的版本号：                               |
|           |                       |commit 4eb78f0a27a85957e1d38a23c5b031cc2aa4b93f                           |
|           |                       |这时就可以执行以下命令取出这个版本：                                      |
|           |                       |git checkout 4eb78f0a27a85957e1d38a23c5b031cc2aa4b93f                     |
|           |                       |执行上述命令后，当前目录里就是这个版本的源码；                            |
|           |                       |要想提取出最新的代码，执行：                                              |
|           |                       |git checkout master                                                       |
+-----------+-----------------------+--------------------------------------------------------------------------+


========= ==================== ========================================================================
 GIT命令                  说明					                                                   示例
========= ==================== ========================================================================
   clone  克隆，从远程下载仓库	git clone https://e.coding.net/weidongshan/01_all_series_quickstart.git
    pull  拉取，从远程更新仓库	                                                        git pull origin
     log    查看本地仓库的记录	                                   git log，快捷键：f前翻、b后翻、q退出
  status     查看本地仓库状态，		                                                         git status
                 比如有无修改，                                                                        
          修改有无提交进仓库里                                                                        
     tag  查看标签，或是打标签                                                  git tag     // 查看标签
                                                                                  git tag v2  // 打标签
checkout        提取出某个版本                               使用git log查看版本，可以看到这样的版本号：
                                                        commit 4eb78f0a27a85957e1d38a23c5b031cc2aa4b93f
                                                                    这时就可以执行以下命令取出这个版本：
                                                  git checkout 4eb78f0a27a85957e1d38a23c5b031cc2aa4b93f                    
                                                          执行上述命令后，当前目录里就是这个版本的源码；
                                                                            要想提取出最新的代码，执行：
                                                                                    git checkout master
========= ==================== ========================================================================

如果只是使用GIT来下载代码，看后面的示例就可以了。如果要深入学习GIT，用GIT来管理你的代码、协同开发，这有一个图形化介绍GIT的网站：https://learngitbranching.js.org/?demo=&locale=zh_CN


3. 使用示例
===========
使用git下载资料，需要先知道git仓库的地址。
以裸机视频GI仓库为例，它的地址是：
https://e.coding.net/weidongshan/noos/doc_and_source_for_mcu_mpu.git
注意：coding的GIT仓库地址无法使用浏览器直接打开。
启动Git Bash后，执行``克隆``命令，就会得到一个名为 ``doc_and_source_for_mcu_mpu`` 的目录：

.. code-block:: console
    :linenos:
	
    $ git clone https://e.coding.net/weidongshan/noos/doc_and_source_for_mcu_mpu.git


如果在你 ``克隆`` 之后，我们又更新了源码，你可以先进入该目录，然后更新。
启动git bash后，使用cd命令可以切换目录。假设要进入D:\abc\doc_and_source_for_mcu_mpu目录，可以执行以下命令：

.. code-block:: console
    :linenos:
	
    $ cd  /D
    $ cd abc
    $ cd doc_and_source_for_mcu_mpu

也可以执行一个命令直接进入该目录，注意目录分隔符是 ``/`` 而非 ``\`` 。

.. code-block:: console
    :linenos:
	
    $ cd  /D/abc/doc_and_source_for_mcu_mpu

在doc_and_source_for_mcu_mpu目录下，执行以下命令获得最新版本。

.. code-block:: console
    :linenos:
	
    $ git pull origin


下图是在Windows上使用git下载、查看、更新源码的操作步骤。

**注意**：建议下载源码后，复制到其他目录去修改；否则以后更新时可能会和你的本地修改产生``冲突``。


3.1 第1天 下载源码
---------------------
假设你要把源码下载到D盘abc目录，如下图操作：

.. figure:: http://photos.100ask.net/100ask/products/tools/Software/git/how_to_use_git/git_day1.png
   
  第1天先下载源码

3.2 第2天 查看无更新
---------------------

.. figure:: http://photos.100ask.net/100ask/products/tools/Software/git/how_to_use_git/git_day2.png
   
  第2天查看无更新

3.2 第3天 查看有更新
---------------------

.. figure:: http://photos.100ask.net/100ask/products/tools/Software/git/how_to_use_git/git_day3.png
   
  第3天查看有更新

注意：不执行 ``git remote show origin`` 查看状态，而是直接执行 ``git pull origin`` 也是可以的，后面这个命令会自动检查，有更新它就会下载更新部分，没有更新也会提示你，如下图：

.. figure:: http://photos.100ask.net/100ask/products/tools/Software/git/how_to_use_git/git_day3_1.png
   
  多次执行提示“已更新”


------------

4. 关于百问网(韦东山)
=========================

 :doc:`/AboutUs/aboutus/index`
 