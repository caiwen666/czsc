# 作业提交

## 黑箱评测

信息学竞赛的题目和我们以往做的数学物理题不一样，信竞题目需要你写代码。评分的时候，没有人会去看你代码怎么写的，而是会有很多测试数据，由评测网站自动将测试数据输入到你的程序，然后将你的程序的输出和标准答案进行比对，完全一致的话就通过这个测试点获得测试点对应的分数，有一个地方不一样，该测试点计 0 分。最终一道题目的得分就是每个测试点的得分相加。

评测你的代码的时候，你的代码就像是一个黑盒子一样，我们不知道也不关心黑盒子里的东西。我们只会把一个测试数据放到这个“黑盒子”，然后你的黑盒子会输出一些数据，然后我们进行比对。这就是黑箱评测。

我们把评测网站简称为 OJ。我们会在 OJ 上做题。比较主流且大型的 OJ 是洛谷：https://www.luogu.com.cn 。洛谷上有非常多的练习题可以供同学们自行练习。

## 注册账号

本次课程的所有题目都在 HydroOJ 上。我们首先需要在 HydroOJ 上注册一个账号：https://hydro.ac 并登录。然后我们打开网址：https://hydro.ac/d/czsc/domain/join ，会来到这个界面：

![](http://pic.caiwen.work/i/2025/07/04/68676eab91f9d.png)

邀请码为：`what_is_dijkstra`，然后点击加入。

为了方便我们追踪同学们的学习情况，请在右上角的下拉菜单中点击图中标记出来的地方：

![](http://pic.caiwen.work/i/2025/07/04/68676f7ea3e54.png)

然后在这里填入你的真实姓名：

![](http://pic.caiwen.work/i/2025/07/04/68676fa220d83.png)

然后点击保存所有更改。

## 题目提交

在 https://hydro.ac/d/czsc/p 中可以看到本次课程的所有例题和作业题。点进去之后可以提交代码，提交代码后网站会自动进行评测并打分。

## 测试点状态

提交题目后会来到评测界面，评测界面会显示你的代码对于每个测试点的通过情况。一个测试点一般会有如下状态：

* Accepted（AC）：测试点通过，获得测试点分数。
* Wrong Answer（WA）：你的程序输出和标准答案不一致，你的程序可能写错了。该测试点计 0 分。
* Runtime Error（RE）：一般是你的数组开小了（第三节课会讲数组）。该测试点计 0 分。
* Time Limit Error（TLE）：超出了时间限制，你可能要考虑效率更高的做法（第六节课会讲时间限制）。该测试点计 0 分。
* Memory Limit Error（MLE）：超出空间限制，你可能要考虑更加节省内存空间的做法（第五节课会讲空间限制）。该测试点计 0 分。