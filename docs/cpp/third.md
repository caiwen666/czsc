# 三 循环结构

我们的程序目前基本能做很多事了，可以输入输出，进行数据的处理，还能根据数据的实际情况进行不同的处理。但我们目前还无法实现这样一个需求：批量处理，比如输出若干个数字，然后求出这些数字的平均数。仅仅使用先前学到的知识，我们的程序只能输入固定数量的数字，且有几个数字我们就需要写多少行代码对齐进行输入和处理。为了解决这个问题，我们就需要学习循环结构。

## 1 数组

我们之前，要创建多少个变量，就要写多少行代码。如果需要创建的变量很多，那么即使我们可以把变量声明写到一行代码上，也很麻烦。于是就有了**数组**来给我们提供遍历：

什么是数组？如果我们把变量看作一个单个的容器，那么数组就可以看作是一个有若干个储物间的柜子。每个储物间都有一个编号，然后根据编号来存放数据。

定义方法：和定义变量类似，但是在变量名后面加一个方括号，方括号里写数组的长度，于是这个变量就成为了一个数组，如：`int arr[10];` 就创建了一个长度为 10 的数组。根据之前的比喻，我们可以理解为创建了一个有 10 个储物间的柜子。

定义完数组之后我们就需要考虑怎么去使用了。数组的使用和变量一样，但是也需要在数组名后面加上方括号，方括号里写明我要操作的是数组的哪个位置，或者说我们要对编号为什么的储物间进行存取数据。如 `arr[1]=arr[2]+arr[3];`。方括号里

大概讲完数组的基本用法，我们需要强调数组的一些注意事项：

使用数组的时候，方括号里的数字我们称之为数组的**下标**或是**角标**。数组的下标是从0开始，换句话说，数组的第一个“储物间”的编号为 0 而不是 1。

定义数组的时候，数组设置了多大，我们就只能使用到多少的“储物间”。再结合数组下标从 0 开始的约定，我们有，如果数组大小为 $n$，那么数组下标的最大值为 $n-1$。比如我们 `int a[3];`，那么我们使用数组的时候只能写 `a[0]`、`a[1]`、`a[2]`，而不能写 `a[3]`。如果数组的大小只有 $n$，而我们使用了大于等于 $n$ 的下标，那么我们就**数组越界**了。或是我们用一个负数作为数组下标，也算**数组越界**。数组越界是一个特殊的错误，他不算一个语法错误，这也就意味着我们在 Dev-C++ 中按下 F11 后不会像少加分号一样立刻报错。而是会在程序运行过程中，如果发生了数组越界，程序将会立刻崩溃，反馈在评测结果上则为“RE（Runtime Error）”。由于操作系统的原因，我们平时在自己的电脑，包括学校的电脑上，如果程序在运行过程中如果数组越界的比较“小”，可能程序仍能继续运行，但是可能会潜在 Bug。但我们在正式竞赛的时候，一旦程序发生数组越界，那么程序将会立刻崩溃，且当前测试点被判为 0 分。

还记得吗？我们在上一节课提到，局部变量的默认值为随机数据。我们现在了解了数组，数组本身也可以视为一个变量。如果我们把数组定义为局部变量，那么数组的默认数据（或者说是数组各个下标位置的数据）为随机数据。相反地，如果数组开为全局变量，则数组默认数据为 0。

局部变量的数组不能开太大，太大的数组需要开成全局变量。如下面的代码：

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() { 
	int a[10000000];
	cout << "okok"; 
	return 0; 
}
```

运行上面的代码，我们会发现，程序还没有输出 `okok` 就退出了，我们的程序实际上是崩溃了。而我们选择把数组 `int a[10000000];` 放到 `int main() { ` 前面，程序就能正常输出 `okok` 了。

综合上述两点，我们还是建议数组一律开成全局变量，除非我们的数组真的很小，比如长度只有 `3` 或 `4`。

还有一个问题，数组的大小定为多少比较好？一般正规的题目中会描述数据的范围，我们根据数据的上限来开数组。一般来说数组最大可以开到 $10^8$。为了避免一不小心数组越界，直接得 0 分了，我们在开数组的时候往往还要开的稍大一点。比如根据题目的数据范围，我们数组开到 $10^6$ 就能解决问题，但我们还是开大一点比较好，有 `int arr[1000006];`。

## 2 循环语句

数组一般和循环语句结合使用，发挥很大的作用。

### 2.1 新的运算符

我们先引入一些新的 C++ 运算符：

* `i++` 表示直接把 `i` 加上1，等价于 `i=i+1`。
* `i--` 同理。
* `++i` 和 `--i` 类似上面两个，我们这里先不去区分。
* `i+=n` 表示直接把 `i` 加上 `n`，等价于 `i=i+n`。
* `i-=n` `i*=n` `i/=n` `i%=n` 同理。

### 2.2 while 语句

语法：

`while(条件){}`

表示：先去判断条件是否满足，如果条件满足，那么就去执行花括号里的代码。执行完之后再去判断条件是否满足，如果满足则再执行花括号里的代码，再继续重复下去，直到条件变得不满足了，while 语句结束。

比如我们可以有如下代码：

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() { 
	int cnt = 0; 
	while (cnt != 10) {
		cout << "[" << cnt + 1 << "]hello, world" << endl;
		cnt ++;
	}
	return 0; 
}
```

上述代码中，我们用 `cnt` 变量记录当前已经输出了几行。`while (cnt != 10) {` 表示 `cnt` 不为 `10` 就继续循环执行 while 语句，换句话说，while 语句需要执行 10 次，这也意味着，我们会输出 10 行内容。运行代码，程序确实输出了 10 行。

有一个特殊的条件：`true`，表示永远成立的条件。对应的， `false` 为永远不成立的条件。

于是我们得到一个特殊的语句：`while(true){}` 则表示一个“死循环”，如：

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() { 
	while (true) {
		cout << "hello, world!" << endl;
	} 
	return 0; 
}
```

我们的程序就会不停地在屏幕上输出文字。

然后我们引入两个控制循环的语句：

`break;` 表示跳出当前循环。比如我们可以有这样的代码：

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() { 
	int cnt = 0; 
	while (true) {
		cout << "hello, world!" << endl;
		cnt ++;
		if (cnt == 10) {
			break;
		}
	} 
    cout << "okok!";
	return 0; 
}
```

首先是一个“死循环”，会不断执行花括号里的代码。但是每次输出后都会将 `cnt` 变量加一。如果 `cnt` 变为 `10`,说明我们输出了 10 次了，那么 if 语句条件成立，执行了 `break;`,跳出了 while 循环。跳出循环后代码继续执行，输出了 `okok`。

`continue;` 表示跳过本次循环的后续代码。

如：

```cpp linenums="1"
#include<bits/stdc++.h>
using namespace std;

int main() { 
	int now = 0; 
	while (true) {
		now ++;
		if (now % 2 == 0) {
			continue;
		}
		cout << "hello, world!" << now << endl;
		if (now >= 10) {
			break;
		}
	} 
	cout << "okok" << endl; 
	return 0; 
}
```

这段代码中的 `now` 变量表示当前循环是第几次循环。每次循环都把 `now` 变量加上一。然后判断一下当前循环次数是否为偶数，如果是偶数，那么就执行 `continue;`，就跳过本次循环后续的代码。注意，只是跳过本次循环，而不是结束当前循环，循环仍然继续。只有当前循环次数为奇数才会执行到第 11 行。同时 12 到 14 行代码表明循环次数不会超过 10。于是上述代码输出为：

```text
hello, world!1
hello, world!3
hello, world!5
hello, world!7
hello, world!9
hello, world!11
okok
```

`continue;` 和 `break;` 只能在 while 和 for（我们稍后会讲）语句内使用。和 if 语句一样，while 语句也能嵌套，如果有多个循环语句嵌套，那么 `continue;` 和 `break;` 语句控制最近的循环。

然后我们看向我们从来没有结束过的语句 `return 0;`。这个语句你目前可以理解为是直接结束程序。如：

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() { 
	int cnt = 0; 
	while (true) {
		cout << "hello, world!" << endl;
		cnt ++;
		if (cnt == 10) {
			return 0;
		}
	} 
    cout << "okok!";
	return 0; 
}
```

运行代码，我们会发现输出了 10 行之后执行了 `return 0;` 程序立刻结束，后面的 `okok` 都没有输出。与上面使用 `break;` 的代码进行比较可以更好的理解。

### 2.3 for 语句

for 语句稍显复杂，但是是最常用的：

`for(初始化语句;条件;循环后执行语句){}`

意思为：先执行一下初始化语句，然后判断一下条件是否成立，如果成立的话就执行花括号的代码，花括号的代码执行完了之后，执行循环后执行语句，然后再判断条件是否成立...这么循环下去。

上述的语句可以大致等价于：

```cpp
初始化语句;
while(条件){
    ...
    循环后执行语句;
}
```

一般而言，我们会在初始化语句里定义变量。注意，初始化语句中定义的变量的作用域仅限于 for 语句中，也就是你不能在 for 循环的外面使用初始化语句定义的变量。

如：

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() { 
	int n;
	cin >> n;
	for (int i=1; i <= n; i++) {
		cout << "hello, world!" << endl;
	}
	return 0; 
}
```

我们首先输入变量 `n`，然后开始了 for 循环：首先定义了一个变量 `i`，初始值为 `1`，然后一直循环，每次循环后 `i` 增加一，直到 `i <= n` 不成立，即 `i > n` ，循环跳出。我们发现，在循环内中，`i` 会从 `1` 开始，变到 `2`，变到 `3`，这么一直增加下去，一直增加到 `n`。`i` 在区间 $[1,n]$ 上**遍历**。

我们从“遍历”的角度去看待 for 语句，有如下例子：

* `for(int i=1;i<=n;i++){}` 从 1 循环到 n、循环 n 次、i 在区间 $[1,n]$ 上遍历。
* `for(int i=1;i<=10;i++){}` 从 1 循环到 10、循环 10 次、i 在区间 $[1,10]$ 上遍历。
* `for(int i=3;i<=13;i++){}` 从 3 循环到 13、循环 11 次、i 在区间 $[3,13]$ 上遍历。
* `for(int i=l;i<=r;i++){}` 从 l 循环到 r 、循环 $r-l+1$ 次、i 在区间 $[l,r]$ 上遍历。
* `for(int i=r;i>=l;i--){}` 从 r 倒着循环到 l ，i 在区间 $[l,r]$ 上倒着遍历。

和 while 语句一样，都有 `continue;` 和 `break;` 来控制循环。并且都能自由嵌套。

## 3 题目选讲

### 3.1【例3.1】区间加问题

https://hydro.ac/d/czsc/p/P1015

这是我们在正式竞赛中看到题目的样子，包含题目描述，输入格式，输出格式，样例，样例说明和数据范围。

首先我们需要考虑怎么读入和存放题目中给定的数列。我们可以考虑使用数组，`in[i]` 就表示数列中第 $i$ 个数。数组大小根据题目数据范围决定，我们发现 $n$ 最大为 $5\times 10^5$。那么我们就有 `int in[500005];`。

然后我们使用循环语句来读入数据：

```cpp
int n,m;
cin>>n>>m;
for(int i=1;i<=n;i++){
    cin>>in[i];
}
```

变量 `i` 在区间 $[1,n]$ 上遍历，把输入的数据分别存放到 `in[1]`、`in[2]`、`in[3]` ... `in[n]` 中。

然后我们读入操作：

```cpp
for(int i=1;i<=m;i++){
    int op,x,y;
    cin>>op>>x>>y;
    if(op==1){
        // 把第 x 个数字加上 y
    }else{
        // 输出第 x 个数到第 y 个数之和
    }
}
```

考虑如何处理操作，对于第一个操作，我们直接有 `in[x]+=y;` 就好了。对于第二个操作，我们还需要再开一个循环，把第 x 个数到第 y 个数每个数都加起来，并输出：

```cpp
int sum=0;
for(int j=x;j<=y;j++){
    sum+=in[j];
}
cout<<sum<<endl;
```

值得注意的是，由于外面的大循环已经使用了变量 `i` 了，那么我们内层嵌套的小循环就为了防止重名，改使用变量 `j` 了。

总结起来就是：

```cpp
#include<bits/stdc++.h>
using namespace std;
int in[500005];
int main() { 
	int n,m;
	cin>>n>>m;
	for(int i=1;i<=n;i++){
	    cin>>in[i];
	}
	for(int i=1;i<=m;i++){
	    int op,x,y;
	    cin>>op>>x>>y;
	    if(op==1){
	        in[x]+=y;
	    }else{
	        int sum=0;
			for(int j=x;j<=y;j++){
			    sum+=in[j];
			}
			cout<<sum<<endl;
	    }
	}
	return 0; 
}
```

注意，尽管数组的下标是从 0 开始，但我们代码中似乎没有用到 `in[0]`。很多时候我们为了方便，根据题目的实际含义，下标从 1 开始使用。但是这么做之前需要确保我们的数组大小要至少多开一个，不然数组就越界了。

但是上述代码我们无法获得满分，并不是因为 WA，而是 TLE（Time Limit Error）。原因是我们上述代码运行的效率比较低，数据量比较大的情况下，代码无法在规定的时间内计算出答案。事实上，我们需要使用一个叫做树状数组的数据结构才能通过本题，而关于数据结构的更多内容需要我们后面的学习。目前我们只需要通过数据量较小的测试点就可以了。

### 3.2【例3.2】判断素数

https://hydro.ac/d/czsc/p/P1005

首先回顾一下我们在小学时学习的概念：

**因数**：如果一个数 $x$ 能够整除 $n$，那么 $x$ 就是 $n$ 的因数。如 $7$ 就是 $14$ 的因数。一个显然的一点是，对于任何大于 $1$ 的数字都一定存在两个因数：$1$ 和他本身。如 $1$ 和 $14$ 是 $14$ 的因数。

**质数/素数**：如果一个数字不存在除了 $1$ 和它本身以外的因数，那么这个数就是质数。$14$ 不是质数，因为除了 $1$ 和 $14$ 以外，还有 $2$ 和 $7$ 两个因数。$5$ 就是质数，因为除了 $1$ 和 $5$ 以外，你找不到其他能整除他的数字，也就是 $5$ 没有除了 $1$ 和 $5$ 以外的因数。特殊地，$1$ 不是质数。

那么对于这道题，我们一个大概的思路就是，先开一个循环，从 $2$ 遍历到 $n$，然后对于每次遍历到的数字 $i$，再开一个循环去判断它是不是素数：从 2 循环到 $i-1$，如果区间 $[2,i-1]$ 内存在整数可以整除 $i$，那么 $i$ 就不是素数。

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() { 
	int n,ans=0;
	cin>>n;
	for(int i=2;i<=n;i++){
		int flag=1;
		for(int j=2;j<=i-1;j++){
			if(i%j==0){
				flag=0;
				break;
			}
		}
		if(flag==1){
			ans++;
		}
	}
	cout<<ans;
	return 0; 
}
```

值得注意的是，我们使用了一个 `flag` 变量，其为 `1` 时表示当前枚举到的数字 `i` 为质数。我们在内层循环判断时，如果在 $[2,i-1]$ 上找到了 $i$ 的因数，那么就置 `flag` 为 `0` 表示 `i` 不是质数，然后结束最内层的循环（因为没有继续判断的必要了）。判断循环结束之后，我们根据 `flag` 的值更新 `ans`。

### 3.3【例3.3】数字切割

https://hydro.ac/d/czsc/p/P1006

要做这个题，我们需要解决一个子问题：如何把一个数字的各个位数取出。我们上节课讲了一个把三位数各个位数取出的题目，并给出了“数字切割”的方法：对 10 取模，再除 10，如此反复。但是上节课是 3 位数，我们就可以手动写代码拆数位。而这次数字的位数不是固定的，我们就需要用循环来解决了：

```cpp linenums="1" hl_lines="8-13"
#include<bits/stdc++.h>
using namespace std;

int main() { 
	int l,r,ans=0;
	cin>>l>>r;
	for(int i=l;i<=r;i++){
		int s=i;
		while(s!=0){
			int d=s%10;
			s/=10;
			if(d==2) ans++;
		}
	}
	cout<<ans;
	return 0; 
}
```

核心部分为标出部分。首先，因为后续对数字除 10 会改变数字，直接作用在变量 `i` 上的话，会影响到循环，所以我们需要把 `i` 先复制到变量 `s` 上。

对一个数字不断地除以 10，那么这个数字会一直减小，直到减小到 0 为止。只要 `s` 不为 0 ，那么 `s` 就还剩余数位需要拆分。因此 while 循环的条件就是 `s!=0` 。后面，变量 `d` 就是本次循环拆分出来的数位。

## 4 总结

* 新的运算符：`+=`、`-=`、`*=`、`/=`、`%=`、`i++`、`i--`、`++i`、`--i`
* 数组
    * 下标从 0 开始
    * 数组越界
    * 数组最好开成全局变量
    * 根据数据范围开数组，并稍微开大一点
* 循环语句
    * while 语句
    * for 语句
        * 初始化语句中创建的变量作用域仅限 for 语句
        * 从在区间上遍历的角度理解 for 语句
    * `continue;`
    * `break;`
    * `return 0;`
* 素数
* 数位切割

## 5 作业

请再次独立做一遍本节题目选讲部分的题目：

* **【例3.1】区间加问题** https://hydro.ac/d/czsc/p/P1004
* **【例3.2】判断素数** https://hydro.ac/d/czsc/p/P1005
* **【例3.3】数字切割** https://hydro.ac/d/czsc/p/P1006

作业题目：

* **【作业3.1】数列求和** https://hydro.ac/d/czsc/p/P1007
* **【作业3.2】打分** https://hydro.ac/d/czsc/p/P1008
* **【作业3.3】校门外的树** https://hydro.ac/d/czsc/p/P1009
* **【作业3.4】珠心算测验** https://hydro.ac/d/czsc/p/P1010