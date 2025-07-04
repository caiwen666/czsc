---
theme: frankfurt
infoLine: true
author: '湖南大学 信息科学与工程学院 李知夏'
title: '分支结构'
date: '2025年7月10日'
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
colorSchema: light
---

# 顺序结构

### CZSC2025 第二讲

---
section: 分支语句
transition: fade-out
---

# 基本语法

<v-click>

分支语句语法：

$$
if(条件)\{...\}
$$

</v-click>

<v-click>

<br>

```cpp
if(条件1){
    cout << "条件1成立！";
}
```

</v-click>

---
transition: fade-out
layout: two-cols
---

# 条件

条件怎么写？

<v-clicks depth="2" class="pr-10">

* `==`：判断是否相等，`a==b`
    * `=`：赋值
    * `==`：判等

* `!=`：判断是否不相等，`a!=b`

* `> < >= <=`：分别表示判断大于，小于，大于等于，小于等于
    * 不能连用。位于闭区间 $[2,3]$ 的条件：`2 <= x <= 3`（错误） `3 >= x >= 2`（错误）

* `&&`：与，将两个条件连接，两个条件都成立才可以
    * 位于闭区间 $[2,3]$ 的条件：`2 <= x && x <= 3`
    * 可以连用：`a == b && b == c && c == d`

</v-clicks>

::right::

<div class="mt-28"></div>

<v-clicks>

* `||`：或，将两个条件连接，两个条件有一个成立就可以
    * 位于区间 $(-\infty,2)\cup [3,+\infty)$ 的条件：`x < 2 || x >= 3`

* `!`：取反
    * 放在一个条件的前面
    * 并且新条件和旧条件的成立情况相反。`!(a>b)` 等价于 `a <= b`

</v-clicks>

<v-click>

灵活运用：`(a==b && b==c) || (a>0 && b>0 && c>0)`

</v-click>

---
transition: slide-left
layout: two-cols
---

# 更多

<div class="pr-10">

<v-click at="2">

````md magic-move
```cpp {*|*|*|*}
if(a > 0){
    cout << "a>0" << endl;
    if(b > 0){
        cout << "b>0" << endl;
    }
}
```
```cpp {*|*}
if(a > 0){
    cout << "a>0" << endl;
}else{
    cout << "a<=0" << endl;
}
```
```cpp
if(a > 3){
    cout << "a>3" << endl;
}else if(a>0){
    cout << "a>0" << endl;
}else if(a>-2){
    cout << "a>-2" << endl;
}
```
```cpp
if(a > 3){
    cout << "a>3" << endl;
}
if(a>0){
    cout << "a>0" << endl;
}
if(a>-2){
    cout << "a>-2" << endl;
}
```
```cpp
if(a > 3){
    cout << "a>3" << endl;
}
if(a>0){
    cout << "a>0" << endl;
}
if(a>-2){
    cout << "a>-2" << endl;
}
// -> a=4
```
```cpp
if(a > 3){
    cout << "a>3" << endl;
}
if(a>0){
    cout << "a>0" << endl;
}
if(a>-2){
    cout << "a>-2" << endl;
}
// -> a=4
// a>3
// a>0
// a>-2
```
```cpp
if(a > 3){
    cout << "a>3" << endl;
}else if(a>0){
    cout << "a>0" << endl;
}else if(a>-2){
    cout << "a>-2" << endl;
}
// -> a=4
```
```cpp {*|*}
if(a > 3){
    cout << "a>3" << endl;
}else if(a>0){
    cout << "a>0" << endl;
}else if(a>-2){
    cout << "a>-2" << endl;
}
// -> a=4
// a>3
```
```cpp
if(a > 3){
    cout << "a>3";
}else if(a>0){
    cout << "a>0";
}else if(a>-2){
    cout << "a>-2";
}else{
    cout << "a<=-2";
}
```
````

</v-click>

</div>

::right::

<div class="mt-28"></div>

<v-click at="1">

* if 语句可以嵌套使用

</v-click>

<v-click at="3">

* 附加一个 else 部分

</v-click>

<v-click at="5">

* 一个或多个 else if

</v-click>

<v-click at="12">

* else 部分也可以加到最后

</v-click>

---
transition: fade-out
section: 再谈变量
layout: two-cols
---

# 变量的作用域

引入了 if 语句之后，代码里出现花括号。花括号会带来问题...

<div class="mr-8" v-click="1">

````md magic-move {lines: true}
```cpp {*|*|*|4-7|4-7}
int a;
cin >> a;
if (a > 0) {
    if (a > 2) {
        int b;
        cin >> b;
    }
    cout << a + b;
}
```
```cpp {*|3-11|4,10}
int a;
cin >> a;
if (a > 0) {
    int c;
    cin >> c;
    if (a > 2) {
        int b;
        cin >> b;
    }
    int c = 1;
}
```
```cpp
int a;
cin >> a;
if (a > 0) {
    if (a > 2) {
        int a;
        cin >> a;
    }
}
```
````

</div>

::right::

<div class="mt-28"></div>

<Item title="作用域" v-click="2">

变量其作用的范围。作用域根据花括号划分，一个变量的作用域为最小包含它的花括号的区域内。

</Item>

<div v-click="4">

* 在不同作用域，变量名可以重复。在相同的作用域中，变量名不能重复

</div>

<div v-click="9">

* 如果有多个重名的，看最近的那个

</div>

---
transition: fade-out
---

# 全局变量

