---
theme: frankfurt
infoLine: true
author: '湖南大学 信息科学与工程学院 李知夏'
title: '顺序结构'
date: '2025年7月10日'
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
colorSchema: light
---

# 顺序结构

### CZSC2025 第一讲

---
preload: true
transition: fade-out
section: '课程介绍'
---

# 要学什么

<div 
  v-click="[1,7]"
  v-motion
    :click-1="{ marginTop: 140, fontSize: '48px', textAlign: 'center' }"
    :click-2="{ marginTop: 0, textAlign: 'left', fontSize: '20px' }"
>
  信息学竞赛<span v-mark.red="6">（算法竞赛）</span>
</div>

<div 
  v-click="[3, 7]"
  class="mt-38 text-6xl text-center"
>
  <span 
    v-motion
      :click-3="{color: 'black'}"
      :click-4="{color: '#3333B3'}"
  >
    C++基础
  </span>
  与
  <span v-mark.red="6">
    <span 
      v-motion
        :click-4="{color: 'black'}"
        :click-5="{color: '#3333B3'}"
    >
      算法
    </span>
  </span>
</div>

---
transition: fade-out
---

# 人员介绍

## 李知夏

<br>

<div v-click>

* 沧州市第一中学 2021级 北大班

</div>

<br>

<div v-click>

* 湖南大学 计算机科学与技术（拔尖计划）

</div>

<br>

<div v-click>

* CCF 第 36 次专业级软件能力认证（CSP）430分（全国前0.36%）
* 2023 年全国青少年信息学奥林匹克联赛（NOIP）一等奖
* 2023 年 CSP 非专业级软件能力认证（提高组）一等奖
* ICPC 国际大学生程序设计竞赛 全国邀请赛（南昌）铜牌

</div>

---
transition: fade-out
layout: two-cols
---

# 人员介绍

<div v-click>

## 金子植

</div>

<br>

<div v-click>

* 沧州市第一中学 2024级 北大班
* CCF 程序设计能力等级 7级
* 2024 年全国青少年信息学奥林匹克联赛（NOIP）一等奖
* 2024 年 CSP 非专业级软件能力认证（提高组）一等奖
* 2023 年 CSP 非专业级软件能力认证（入门组）一等奖
* 2022 年 CSP 非专业级软件能力认证（入门组）一等奖
* 2020 年 CSP 非专业级软件能力认证（入门组）一等奖

</div>

::right::

<div class="mt-28"></div>

<div v-click>

## 付鹏汇

</div>

<br>

<div v-click>

* 沧州市第一中学 2021级 北大班
* 浙江工业大学 健行学院 数智实验班
* ICPC 国际大学生程序设计竞赛 全国邀请赛（西安）金牌

</div>


---
transition: fade-out
layout: two-cols
---

# 人员介绍

<div v-click>

## 留昊

</div>

<br>

<div v-click>

* 沧州市第一中学 2021级
* 西安理工大学 计算机科学与技术
* ICPC 国际大学生程序设计竞赛 全国邀请赛（西安）银牌
* ICPC 国际大学生程序设计竞赛 全国邀请赛（东北）银牌
* CCF 第 36 次专业级软件能力认证（CSP）400分
* 2023 年全国青少年信息学奥林匹克联赛（NOIP）二等奖
* 2023 年 CSP 非专业级软件能力认证（提高组）二等奖

</div>

::right::

<div class="mt-28"></div>

<div v-click>

## 赵玉航

</div>

<br>

<div v-click>

* 沧州市第一中学 2018级
* 北京邮电大学 软件工程
* CCPC 中国大学生程序设计竞赛（绵阳） 银牌
* ICPC 国际大学生程序设计竞赛 亚洲区域赛（杭州） 铜牌
* 蓝桥杯全国软件和信息技术专业人才大赛 B组 国家一等奖
* 2019 年 CSP 非专业级软件能力认证（提高组）二等奖

</div>

---
transition: fade-out
layout: two-cols
---

# 人员介绍

<div v-click>

## 王添翼

</div>

<br>

<div v-click>

* 沧州市第一中学 2020级
* 福建师范大学 网络安全
* 蓝桥杯全国软件和信息技术专业人才大赛 B组 省级一等奖
* 2021 年 CSP 非专业级软件能力认证（提高组）二等奖

</div>

::right::

<div class="mt-28"></div>

<div v-click>

## 张博雄

</div>

<br>

<div v-click>

* 沧州市第一中学 2021级 北大班
* 兰州交通大学 应用物理
* 蓝桥杯全国软件和信息技术专业人才大赛 B组 省级一等奖
* 2022 年 CSP 非专业级软件能力认证（提高组）二等奖

</div>

---
transition: slide-left
---

# 人员介绍

<div v-click>

## 王金轲、孙文芳

</div>

<br>

<v-clicks>

* 沧州市第一中学在职教师
* CCF NOI认证指导教师
* 河北省信息学竞赛优秀指导教师

</v-clicks>


---
transition: slide-left
---

# 课程资源

<v-clicks>

* 课程回放：课程结束24小时后发布到B站
* 通知群：微信群
* 交流群：QQ群
* 答疑：随时
* <span v-mark.red="10">课程网站：https://czsc.caiwen.work/</span>
  * 讲义、拓展、其他内容...
* 作业提交：https://hydro.ac/d/czsc/
  * 稍后会解释
* 练习：https://www.luogu.com.cn/
* 书籍（可选）
  * 洛谷 《深入浅出程序设计竞赛（基础篇）》 高等教育出版社
  * 《算法竞赛》罗勇军、郭卫斌 清华大学出版社

</v-clicks>

---
transition: fade-out
section: '基础语法'
---

# 第一个程序

<Item title="例1.1 第一个程序">

现在请你编写这样一个程序：计算两个数字的和。向程序中输入 `3 5`，程序会输出 `8`。

</Item>

<div v-click>

```cpp {*}{lines:true}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a;
   	int b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```

</div>

---
transition: fade-out
layout: two-cols
---

# 程序的基本框架

<div class="pr-10">

````md magic-move {lines: true}
```cpp {*|*|1-4,14-15|5-13|5-13|6-7,9-14|6-7,9-14|6-7,9-14|6-7,9-14|6-7,9-14|5,8,11-13}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a;
    int b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() {
    int a;
    int b;
    cin >> a;
    cin >> b;
    int c;
    c = a + b;
    cout << c;
    return 0;
}
```

```cpp {5,8,11-13|5,8,11-13}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a;
    int b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```
````

</div>

<Arrow v-click="[5,10]" x1="260" y1="200" x2="160" y2="235" color="#F44336" />

<Arrow v-click="[5,10]" x1="260" y1="217" x2="160" y2="253" color="#F44336" />

<Arrow v-click="[5,10]" x1="285" y1="251" x2="185" y2="287" color="#F44336" />

<Arrow v-click="[5,10]" x1="285" y1="268" x2="185" y2="304" color="#F44336" />

<Arrow v-click="[5,10]" x1="260" y1="285" x2="160" y2="321" color="#F44336" />

<Arrow v-click="[5,10]" x1="290" y1="304" x2="190" y2="340" color="#F44336" />

<Arrow v-click="[5,10]" x1="290" y1="321" x2="190" y2="357" color="#F44336" />

<Arrow v-click="[5,10]" x1="285" y1="338" x2="185" y2="374" color="#F44336" />


<Arrow v-click="[13,14]" x1="290" y1="121" x2="190" y2="200" color="#F44336" />

<Arrow v-click="[13,14]" x1="400" y1="200" x2="280" y2="320" color="#F44336" />

<Arrow v-click="[14,20]" x1="80" y1="200" x2="100" y2="300" color="#F44336" />

::right::

<div class="mt-28"></div>

<img v-if="$clicks == 1" src="http://pic.caiwen.work/i/2025/06/10/6847eead7199c.png">

<Item title="语句" v-if="$clicks == 4">

每一行代码都是一个**语句**，告诉程序要干什么。程序从上到下依次执行语句。

</Item>

<div v-if="$clicks >=5 && $clicks <=7">

<span v-mark.red="7">每个后面都需要有一个分号！</span>

<img v-if="$clicks == 6 || $clicks == 7" src="http://pic.caiwen.work/i/2025/06/10/6847fa6b0f734.png">

</div>

<div v-if="$clicks >= 8 && $clicks <= 9">

上方：中文符号；下方：英文符号

<img src="http://pic.caiwen.work/i/2025/06/10/6847fb5104325.png">

<img src="http://pic.caiwen.work/i/2025/06/10/6847fbbb70efa.png" v-if="$clicks == 9">

</div>

<Item title="注释" v-if="$clicks >= 10 && $clicks <= 13">

双斜杠 `//` 后面的所有内容表示**注释**。**注释**以双斜杠开始，双斜杠后面的部分都会被忽略，不会被执行。

</Item>

<div v-if="$clicks >= 15 && $clicks <= 19">

每个语句前面这些空白部分是**缩进**

</div>

<img src="http://pic.caiwen.work/i/2025/06/10/68480103cdd16.jpg" v-if="$clicks == 16">

<div v-if="$clicks >= 17 && $clicks <= 19">

并不是必须的，加不加都可以。

</div>

<div v-if="$clicks >= 18 && $clicks <= 19">

````md magic-move {lines: true}
```cpp {*|*|*|*|*|*}
    for(int i=1;i<=n;i++){
			if(a[i]<b[x]){
			continue;
			}
		ans++;
				b[x]=0x3f3f3f3f;
				if(x==m){
				break;
				}
			x++;
	}
```

```cpp {*}
    for(int i=1;i<=n;i++){
		if(a[i]<b[x]){
			continue;
        }
		ans++;
        b[x]=0x3f3f3f3f;
        if(x==m){
            break;
        }
        x++;
	}
```
````

</div>

---
transition: fade-out
layout: two-cols
---

# 数据类型和变量

<div class="pr-10">

```cpp {*|6|6|6|6|6|6|6|6|6|6|6|6|6|6|6|6|6|6|6|6}{lines: true}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a;
    int b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```

</div>

::right::

<div class="mt-28"></div>

<Item title="变量" v-if="$clicks >= 2 && $clicks <= 4">

**变量**你可以理解为是一个可以存放数据的容器。在这里，我们需要把用户输入的数字先给保存起来，然后再进行加法运算。

</Item>

<div v-if="$clicks >=3">

<br v-if="$clicks <= 4">

$$
[数据类型]\space[变量名称];
$$


</div>

<div v-if="$clicks == 4">

<br>

变量一定是要先声明后使用。

</div>

<div v-if="$clicks >= 5 && $clicks <= 9">

C++中所有的数据都有他们自己的类型。

</div>

<div v-if="$clicks >= 6 && $clicks <= 9">

* 整数，用 `int` 来表示。

</div>

<div v-if="$clicks >= 7 && $clicks <= 9">

* 小数，用 `double` 来表示。浮点数。

</div>

<div v-if="$clicks >= 8 && $clicks <= 9">

* 布尔类型，字符类型，字符串类型。

</div>

<div v-if="$clicks == 9">

<br>

```cpp
int aaa; //创建整数变量aaa
double bb; //创建小数变量bb
```

</div>

<div v-if="$clicks >= 10 && $clicks <= 15">

变量的名称可以随便取。但是有下面的规则：

</div>

<div v-if="$clicks >= 11 && $clicks <= 15">

* 不能以数字开头，如 `int 1var;` 

</div>

<div v-if="$clicks >= 12 && $clicks <= 15">

* 不能以特殊字符开头，如 `int ?var;` 

</div>

<div v-if="$clicks >= 13 && $clicks <= 15">

* 变量名不能用中文。

</div>

<div v-if="$clicks >= 14 && $clicks <= 15">

* 有一些名字不能用。如 `int double;`

</div>

<Item title="标识符" v-if="$clicks == 15">

在 C++ 中，除了要给变量取一个名字来方便后面使用外，还有其他的地方也需要我们来自己命名。我们自己起的名字在 C++ 里称为 **标识符**。

</Item>

<div v-if="$clicks >= 16 && $clicks <= 17">

赋值语句语法：

</div>

<div v-if="$clicks >= 17">

$$
[变量]=[变量/字面量];
$$

</div>

<div v-if="$clicks >= 18 && $clicks <= 20">

```cpp
int a;
a=114514; 
```

</div>

<div v-if="$clicks >= 19 && $clicks <= 20">

```cpp
double c;
c=114.514;
```

</div>

<div v-if="$clicks == 20">

```cpp
int a;
int b;
b=1;
a=2;
a=b;
```

</div>

---
transition: fade-out
layout: two-cols
---

# 输入

<div class="pr-10">

```cpp {*|9|9}{lines: true}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a;
    int b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```

</div>

::right::

<div class="mt-28"></div>

<div v-click="2">

从键盘输入:

$$
cin >> [变量];
$$

</div>

---
transition: fade-out
layout: two-cols
---

# 运算

<div class="pr-10">

```cpp {*|12|12|12|12}{lines: true}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a;
    int b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```

</div>

::right::

<div class="mt-28"></div>

<div v-click="2">

* `[变量/字面量]+[变量/字面量];` 把两个数字相加。
* `[变量/字面量]-[变量/字面量];` 把两个数字相减。

</div>

<v-clicks at="3">

* `[变量/字面量]*[变量/字面量];` 把两个数字相乘。
* `[变量/字面量]/[变量/字面量];` 把两个数字相除。

</v-clicks>

<div v-click>

四则混合运算

```cpp
c=(a+b)*(a-b)
```

</div>

---
transition: slide-left
layout: two-cols
---

# 输出

<div class="pr-10">

```cpp {*|13|13|13|13|13|13|13|13|13|13|13}{lines: true}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a;
    int b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```

</div>

::right::

<div class="mt-28"></div>

<div v-if="$clicks >= 2">

<div v-if="$clicks >= 2 && $clicks <= 3">

输出到屏幕上：

</div>

$$
cout << [变量/字面量];
$$

</div>

<div v-if="$clicks == 3">

$$
cin >> [变量];
$$

</div>

<div v-if="$clicks >= 5 && $clicks <= 6">

```cpp
cout << "Hello, World";
```

</div>

<div v-if="$clicks == 6">

**字符串**类型的字面量：用双引号包裹起来

</div>

<div v-if="$clicks >= 7">

```cpp
cout << "sum: ";
cout << c;
```

</div>

<img src="http://pic.caiwen.work/i/2025/06/10/6848154c0a0e1.png" v-if="$clicks == 8" />

<div v-if="$clicks >= 9">

换行符： `endl`

</div>

<div v-if="$clicks >= 10">

```cpp
cout << "sum: ";
cout << endl;
cout << c;
```

</div>

<img src="http://pic.caiwen.work/i/2025/06/10/684815f9402ed.png" v-if="$clicks >= 11" />

---
transition: fade-out
section: 语法深入
layout: center
---

## C++的语法其实可以灵活点...

---
transition: fade-out
layout: two-cols
---

# 变量

<div class="pr-10">

````md magic-move {lines: true}
```cpp {*|6-7|6-7}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a;
    int b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```
```cpp {*|10-11|10-11}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a,b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```
```cpp {*}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a,b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c = a + b;
    cout << c;  // 输出运算结果
    return 0;
}
```
````

</div>

::right::

<div class="mt-28"></div>

<div v-click="2">

可以一个语句声明多个变量：

$$
[数据类型]\space[变量名1],[变量名2],...;
$$

</div>

<div v-click="5">

可以在变量声明的时候就直接赋值

</div>

---
transition: fade-out
---

# 变量

如果一个变量在声明之后，没有对其进行赋值，直接就使用这个变量，那么这个变量中存放的数据是什么？

<div v-click="1">

````md magic-move {lines: true}
```cpp {*|*|*}
#include<bits/stdc++.h>
using namespace std;

int main() {
    int a;
    cout << a; 
    return 0;
}
```
```cpp {*}
#include<bits/stdc++.h>
using namespace std;

int main() {
    double a;
    cout << a; 
    return 0;
}
```
````

</div>

<div v-click="2">

默认值为 `0`？

</div>

<div v-click>

随机：默认值不会得到保证

</div>

<div v-click>

<span v-mark.red="6">你在使用变量时，一定要确定这个变量已经被赋值过了（直接赋值/cin输入）</span>

</div>

---
transition: fade-out
layout: two-cols
---

# 输入输出

<div class="pr-10">

````md magic-move {lines: true}
```cpp {*|8-9|8-9}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a,b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c = a + b;
    cout << c;  // 输出运算结果
    return 0;
}
```
```cpp {*|9-10|9-10}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a,b;
    // 分别从键盘输入这两个数字
    cin >> a >> b;
    int c = a + b;
    cout << c;  // 输出运算结果
    return 0;
}
```
```cpp {*|*}
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a,b;
    // 分别从键盘输入这两个数字
    cin >> a >> b;
    cout << a + b;
    return 0;
}
```
```cpp
#include<bits/stdc++.h>
using namespace std;

int main() {
    int a,b;
    cin >> a >> b;
    cout << a + b;
    return 0;
}
```
```cpp
#include<bits/stdc++.h>
using namespace std;

int main() {
    // 定义两个整形变量
    int a;
   	int b;
    // 分别从键盘输入这两个数字
    cin >> a;
    cin >> b;
    int c;  // 再定义一个变量
    c = a + b;  // 计算 a 与 b 的和并存放到变量 c 中
    cout << c;  // 输出运算结果
    return 0;
}
```
```cpp
#include<bits/stdc++.h>
using namespace std;

int main() {
    int a,b;
    cin >> a >> b;
    cout << a + b;
    return 0;
}
```
````

</div>

::right::

<div class="mt-28"></div>

<div v-click="2">

`<<` 和 `>>` 可以连用

</div>

<div v-click="5">

C++ 语法灵活，变量 `c` 没必要。

</div>

<div v-click="7">

空格和换行符都可以分隔

</div>

---
transition: fade-out
---

# 数据类型

首先我们需要先做一个辨析：

<div v-click>

|字面量|数据类型|
|-|-|
|1|整数（int）|
|1.0|小数（double）|
|"1"|字符串|


</div>

---
transition: fade-out
---

# 数据类型

讨论一下不同数据类型混用的情况

<div>

````md magic-move
```cpp
int a = 11.4514
```
```cpp
int a = 11.4514  // a 为 11
```
````

</div>

<v-clicks>

隐式数据类型转换

double 转为 int 时，小数部分会直接丢失

<hr>

两个同类型数据进行运算，运算结果的类型一致

不同类型？

运算结果为精度更高的类型

</v-clicks>

---
transition: slide-left
layout: two-cols
---

# 数据类型

<div class="pr-10">

````md magic-move
```cpp {*|*|*|*}
int a=3,b=2;
int c=a/b;
cout<<c;
```
```cpp {*}
int a=3,b=2;
int c=a/b;
cout<<c;
// -> 1
```
```cpp {*}
int a=3,b=2;
double c=a/b;
cout<<c;
```
```cpp {*}
int a=3,b=2;
double c=a/b;
cout<<c;
// -> 1
```
```cpp {*}
cout << 3 / 2;
```
```cpp {*}
cout << 3 / 2;
// -> 1
```
```cpp {*}
cout << 3.0 / 2.0;
```
```cpp {*}
cout << 3.0 / 2.0;
// -> 1.5
```
```cpp {*}
cout << 3 / 2.0;
// -> 1.5
```
```cpp {*}
cout << 3.0 / 2;
// -> 1.5
```
```cpp {*|*}
double a=3,b=2;
double c=a/b;
cout<<c;
```
```cpp {*|*}
int a=3,b=2;
double c=a/b;
cout<<c;
```
```cpp {*|*}
int a=3,b=2;
double c=(double)a/b;
cout<<c;
// -> 1.5
```
```cpp {*}
int a=3,b=2;
double c=1.0*a/b;
cout<<c;
// -> 1.5
```
```cpp {*|*|*}
int a=3,b=2;
double c=a/b*1.0;
cout<<c;
// -> 1
```
```cpp {*}
double a=1.0/3,b=4.0/3,c=5.0/3;
printf("%.10lf\n",c);
printf("%.10lf\n",a+b);
printf("%.20lf\n",c);
printf("%.20lf\n",a+b);
```
```cpp {*|*}
double a=1.0/3,b=4.0/3,c=5.0/3;
printf("%.10lf\n",c);
printf("%.10lf\n",a+b);
printf("%.20lf\n",c);
printf("%.20lf\n",a+b);
// 1.6666666667
// 1.6666666667
// 1.66666666666666674068
// 1.66666666666666651864
```
````

</div>

::right::

<div class="mt-28"></div>

<v-clicks at="1">

* double 到 int 隐式数据类型转化有小数损失
* 同类型运算，运算结果类型保持一致
* 不同类型运算，运算结果为精度更高的类型

</v-clicks>

<div v-click="14">

**我们的程序最好把 double 类型的使用控制在一个较小的范围**

</div>

<div v-click="16">

* 显式强制数据类型转换

</div>

<div v-click="18">

<span v-mark.red="21">

* 最前面乘 `1.0` 扩大精度

</span>

</div>

<div v-click="22">

<br>

```cpp
// 保留 5 位数字输出 double 类型 x
printf("%.5lf",x);
```

</div>

<div v-click="25">

计算机在计算无限小数的时候会有偏差

</div>

---
transition: fade-out
section: 结尾
layout: two-cols
---

# 总结

<v-clicks depth="3">

- 程序的基本框架
- 代码基本规则
  - 顺序执行
  - 分号
  - 英文符号
  - 注释
  - 缩进

</v-clicks>

::right::

<div class="mt-28"></div>

<v-clicks depth="3">

- 变量
  - 变量声明
  - 数据类型
    - 隐式数据类型转换
    - 同种/不同种类型运算结果的类型
    - 如何避免运算时小数的丢失
    - 保留小数到指定位数后输出
  - 标识符规则
  - 变量的默认值
- 运算
  - 乘法和除法符号
- 输入与输出
  - 连用 `<<` 和 `>>`
  - 输出字符串字面量

</v-clicks>

---
transition: fade-out
---

# 作业

<v-clicks>

* **【作业1.1】计算器** https://hydro.ac/d/czsc/p/P1000

* **【作业1.2】三角形面积** https://hydro.ac/d/czsc/p/P1001

</v-clicks>

---
transition: fade-out
layout: center
---

# Q&A