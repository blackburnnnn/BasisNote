### 账户&配置

- [GitHub更名奇遇记](https://www.jianshu.com/p/6f2fdba48129)
- [Github提交不显示修复](https://blog.csdn.net/qq_41376740/article/details/120900091)
- SAP Mac
  - 

#### 创建新仓库&推送本地代码

- 将MyCode源代码文件夹初始化为git仓库并上传至github
  1. 初始化 `git init`
  2. 在github创建仓库 <img src="/Users/leizhenhao/Library/Application Support/typora-user-images/image-20220713101135375.png" alt="image-20220713101135375" style="zoom:23%;" />
  3. 创建origin连接 `git remote add origin git@github.com:blackburnnnn/Coding.git`
  4. 同步github空仓库的readme文件 `git fetch` & `git merge`
  5. `git add` & `git commit`
  6. `git push origin master(main)`

#### 拉取代码

- 

#### 命令详解

- `git rebase`
- `git stash`
- [清空工作区和暂存区](https://blog.csdn.net/u014089832/article/details/124074169)：`git checkout` + `git reset`
- [.gitignore简介](https://blog.csdn.net/weixin_45318845/article/details/120740012) 在Git工作区的根目录下创建一个特殊的.gitignore文件，然后把要忽略的文件名填进去，Git就会自动忽略这些文件或目录

#### 开源项目检索

- 搜索
  1. `in:name springboot`
  2. `in:name springboot stars:>3000`
  3. `in:readme springboot stars:>3000`
  4. `in:name springboot stars:>3000 forks:>1000`
  5. `in:description 微服务 language:java pushed:>2019-09-03`

#### 代码合并

- [本地推送代码到github指定分支](https://blog.csdn.net/weixin_57645299/article/details/124433880)：本地的分支名需要和指定分支名相同

#### 运维流程

- 灰度发布(又名金丝雀发布)：是指在黑与白之间，能够平滑过渡的一种发布方式。在其上可以进行A/B testing，即让一部分用户继续用产品特性A，一部分用户开始用产品特性B，如果用户对B没有什么反对意见，那么逐步扩大范围，把所有用户都迁移到B上面来。灰度发布可以保证整体系统的稳定，在初始灰度的时候就可以发现、调整问题，以保证其影响度。灰度发布开始到结束期间的这一段时间，称为灰度期

#### GitHub

- 账户id blackburnnnn，老密码；可以直接调用github api查看用户详细信息

  <img src="/Users/leizhenhao/Library/Application Support/typora-user-images/image-20221003102551051.png" alt="image-20221003102551051" style="zoom: 33%;" />

- 授衔fork原始仓库，然后从自己仓库克隆

- 克隆目标仓库(git@github.com:OpenEduTech/OpenEduKG.git)

- `git remote -v` <img src="/Users/leizhenhao/Library/Application Support/typora-user-images/image-20220914110652659.png" alt="image-20220914110652659" style="zoom:50%;" />

- 最终push命令指定远程仓库名和分支名: `git push origin main`

- 从我的分支(head repository)合并到base分支

  ![image-20220914112254291](/Users/leizhenhao/Library/Application Support/typora-user-images/image-20220914112254291.png)
  
- 增加上游仓库，拉取代码的时候应为main
