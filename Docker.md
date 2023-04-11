> [Docker 1小时快速上手教程](https://www.bilibili.com/video/BV11L411g7U1/?spm_id_from=333.337.search-card.all.click&vd_source=726461adc26f0b0f56256c07f5a478dc)、[Docker从入门到实践](https://yeasy.gitbook.io/docker_practice/image/rm)、[CSDN Docker for Mac](https://blog.csdn.net/qq_39208536/article/details/123357756)

#### Docker安装

- (11/14)Docker满足的需求就是在本地环境开发、测试完成后，打包为Docker镜像(可理解为即插即用的软件安装包)，然后到各种服务器上，只需要通过相同的简单命令就可以部署这个镜像，避免不同服务器环境和本地代码出现各种各样的不适配问题

- 比如想学习一下redis，ElasticSearch，手动安装非常复杂，但是Docker一个命令就可以搞定

- 重要概念：镜像、容器
  镜像：可以理解为软件安装包，可以方便的进行传播和安装。
  容器：**软件安装后的状态，每个软件运行环境都是独立的、隔离的**，称之为容器。

- 使用Dokcer桌面版，账号qq邮箱，密码老密码，再设置Docker Engine为国内的源

- `docker info`  ![image-20221114112528496](/Users/leizhenhao/Library/Application Support/typora-user-images/image-20221114112528496.png)

- Hello World实例

  - `docker image pull library/hello-world` 拉取官方的library/hello-world镜像
  - 拉取完成后 `docker images` 查看本机所有的镜像
  - `docker container run hello-world` 表示在**新容器**中运行指定镜像，`docker container run` 命令会从 image 文件，**生成一个正在运行的容器实例**，且其具有自动抓取 image 文件的功能，如果发现本地没有指定的 image 文件，就会从仓库自动抓取，因此前面的 `docker image pull` 命令并不是必需步骤
  - 有些容器(比如ubuntu服务)在run完了之后不会自动终止，需要手动终止

- 客户端查看已拉取的镜像

  <img src="/Users/leizhenhao/Library/Application Support/typora-user-images/image-20221114113441050.png" alt="image-20221114113441050" style="zoom:50%;" />

#### 软件快速安装

- 