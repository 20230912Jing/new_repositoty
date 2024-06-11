# Github
---
## 关键字查询:
   
   xx (python) awesome: 查找该标签下的xx (python) 项目

   xx (python) tutorial: 查询xx资料，书籍，文档

   xx (socket) sample: 查询对应技术的代码样本

## Github三要素
### Repository 仓库

    仓库是github项目管理存储的基本单位

    一个仓库中存储一个项目，一个用户可以拥有多个仓库，一般仓库分为public, private

### Commit 提交
    
    程序员整个开发周期，有大量的对应代码资源的迭代和修改，都可以通过commit的方式进行记录，便于程序员回溯代码，即是这些代码被删除

    提交便于使用者观察整个工程的开发流程以及设计流程

### Branch 分支

    在仓库中可以包含多个分支，分支才是代码文件的第一存储单元，默认的仓库主分支为master/main

    *不仅可以管理代码存储，还便于多人协作开发

![](https://i.postimg.cc/7L62Kkq6/1.jpg)

## 仓库内容

   Code，资源存储，代码资源，二进制，项目管理脚本，许可证等等

   issues，使用时遇到的bug或进行提交，等待反馈

   README，使用markdown语言编写，工程自述文件，开发进度，版本更新，使用介绍等等

   LICENSE 许可证：GPL2.0，3.0，Apahce 2.0，Mit，这些许可证，给使用者最大的使用权限以及最小的限制

## Git软件，分布式版本控制系统

   仓库管理软件，使用git管理私人代码或者企业代码

![](https://i.postimg.cc/CMmd626n/2.jpg)

## 设备认证
   
   1.如何让网站的账户与设备绑定，后续完成代码的管理，上传下载
```bash
	git init //创建本地仓库  *后续对仓库的操作，都在仓库位置(master)

	git config --list //查看git的配置文件

	git config --global user.email "邮箱"

	git config --global user.name “用户名"  SSH远程访问

	ssh-keygen -t rsa -C "注册邮箱" //创建本地密文

 	*去对应的目录查找密文文件

		rsa.pub 复制密文.粘贴 settings -> SSH key and GPG -> new ssh key -> 粘贴

		ssh -T git@github.com //测试关联是否成功
```

   2.为目标仓库起别名，定位目标仓库，后续上传
```bash
	git remote add origin "ssh地址" //为ssh仓库地址创建别名为origin

	git remote remove origin //删除origin别名

	git remote add origin "ssh地址" //为ssh仓库地址创建别名为origin
```

## 本地设备与云端仓库的交互逻辑

![](https://i.postimg.cc/vHKTGVyQ/3.jpg)

```bash
	git add code.c #添加内容

	#将缓冲区数据提交到本地仓库

	git commit #提交到本地仓库

	git commit -m "备注信息" #生成提交记录

	git push origin master #将本地仓库内容推到云端仓库

	git status #查看状态

	git rm code.c #删除本地文件以及仓库中文件

	git restore code.c #复位误删除文件（仓库存在）
```

## 代码更新的依赖关系被破坏

   本地内容比云端新，完成更新替换，但是如果直接修改云端内容，导致，本地内容无法再次修改

   先拉取git pull 云端内容 与本地内容合并或操作，而后再次推即可

```bash
	git pull --rebase origin master

	git rebase --skip "忽略本地内容 保留云端内容"

	git rebase --about "忽略新版 此时还不能上传"

	git rebase --continue "版本合并，解决冲突后可以直接上传"
```

## 下载开源代码

```bash
	git clone "https仓库地址" #下载开源项目code资源
```

## 分支Branch

   关于分支的相关命令，创建分支、选择分支、合并分支等等

## Markdown，文本修饰语言，用特殊符号修饰正文效果<br>

## 标题修饰符\#

# 标题修饰符(一级标题)
## (二级标题)
### (三级标题)
#### (四级标题)
##### (五级标题)

## 正文内容

   输入正文内容，但是如果需要换行，用\<br\>标签

## 修饰正文
	
   *一段测试文本*

   **一段测试文本**

   ***一段测试文本***

   ~~一段测试文本~~

   这是一段的`关键字`的内容

## 分割线
    
   用\-\-\- 表示分割线

---

## 引用效果用\>表示
> 你自己就是一座金矿，关键在于如何挖掘和利用
>> 苏格拉底
>>> 三级引用
>>>> 四级引用

## 列表修饰符
### 无序列表 \*
* 二次元游戏
  * 原神
    * 克洛琳德
* 大逃杀类
  * PUBG
  * APEX

### 有序列表 1.
1. 物理学
   1. 粒子物理
   2. 原子核物理
   3. 凝聚态物理
2. 计算机科学
   1. 分布式架构
   2. 云计算

### 混合列表
1. 测试一级
   * 测试二级
   2. 测试三级

### 表格
角色|地区|排行
--|:--:|--:|
克洛琳德|枫丹|1
仆人|枫丹|2
神里绫华|稻妻|3

### 代码片段

```c
	#include <stdio.h>
	int main()
	{
		return 0;
	}
```
```cpp
	#include <iostream>
```
```python
	import <os>
```
```bash
	ls -l
	cd
	push
```

### 超链接技术

[Github](https://www.github.com "点击访问")

### 插入图片
![]()
