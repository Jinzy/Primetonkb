# Primeton Knowledge Base
这里是普元公司（Primeton Ltd.）金融事业部的内部知识库。包括了多年来普元面向企业级客户的服务过程中积累的关于或有益于普元产品实施的各方面技术方案、经验技巧以及规范制度。

PrimetonKB由普元所有技术专家共同协作维护。所有人均可下载查阅本知识库内容，并可提交知识点到develop分支，发出pull request后，由知识管理组成员审核通过后，合并到master分支。

## 知识库使用帮助
### 首次使用知识库
#### 1. 准备工作
***
##### 下载并安装git（若已安装，请忽略此步）
*  [git下载地址](https://git-scm.com/downloads "git下载地址")
*  [git安装指南](https://git-scm.com/book/zh/v1/%E8%B5%B7%E6%AD%A5-%E5%AE%89%E8%A3%85-Git "git安装指南")

##### 注册github帐号（若已注册，请忽略此步）
*  访问[github](https://github.com/)，按照提示进行操作
*  完成后在Settings中设置个人基本信息及安全信息，尤其是个人邮箱和SSH Keys

##### 名词解释
*  源库，特指本库，地址为https://github.com/Primeton-Ltd/Primetonkb.git
*  远程库，Fork到你个人github帐号下的仓库，由于此时仓库仍存储于github，因此相对于本机环境，这个库叫远程库
*  本地库，Clone到本地机器硬盘的仓库

#### 2. Fork源库(组织成员请直接进行Clone)
***
非组织成员请访问[源库](https://github.com/Primeton-Ltd/Primetonkb.git)，点击右上角的Fork按钮，按提示操作后，将源库Fork到个人的远程库

#### 3. Clone
***
在本地机器打开git bash，依次执行以下命令：

> git clone https://github.com/yourname/Primetonkb.git       注意：需要将yourname替换为你自己的github帐号，下同。

组织成员：
> git clone https://github.com/Primeton-Ltd/Primetonkb.git
> 
> git remote add origin https://github.com/Primeton-Ltd/Primetonkb.git

非组织成员：
> git clone https://github.com/yourname/Primetonkb.git     <注意：需要将yourname替换为你自己的github帐号，下同>
>>>>>>> ba067aa1237dffd368869d6dbff983500b932519
> 
> git remote add origin https://github.com/yourname/Primetonkb.git
> 
> git remote add upstream https://github.com/Primeton-Ltd/Primetonkb.git

注意：首次Clone耗时较长，请保证有较长时间的联网环境

### 知识分享
#### 1. 提交
***
分享规范：在本地Primetonkb文件夹下进入特定分类文件夹（如应用案例），新建以所分享的知识命名的文件夹，把要分享的内容放在该新建文件夹下即可

在本地机器打开git bash,依次执行以下命令：

组织成员：
> git checkout develop    <新建本地develop分支与源库develop分支的关联并切换到develop分支>
>
> git add .
>
> git commit -m "本次提交备注"
>
>git push -u origin develop

非组织成员：
> git add .
>
> git commit -m "备注"
>
>git push -u origin master

#### 2. Create Pull Request(仅针对非组织成员)
***
进入远程库界面点击New Pull Request，请注意选择base fork:Primeton-LtdPrimetonkb base:develop，点击创建即可，如果该pull request未审核通过，所有后续修改都将追加到这个pull request之后，无需新创建

#### 3. Merge Pull Request(仅针对组织成员)
***
进入源库界面点击Pull Requests进行知识审核，审核通过的选择Merge pull request，未通过的选择Close pull request

### 阅读知识
#### 更新
***
在本地机器打开git bash,依次执行以下命令：

组织成员：
> git checkout master
>
>git fetch origin master
>
>git merge origin master

非组织成员：
> git fetch upstream master
>
>git merge upstream master

