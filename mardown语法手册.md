mardown语法

## 标题

```
# 这是一级标题
## 这是二级标题
### 这是三级标题
#### 这是四级标题
##### 这是五级标题
###### 这是六级标题
```



## 字体

```
**这是加粗的文字**
*这是倾斜的文字*`
***这是斜体加粗的文字***
~~这是加删除线的文字~~
==这是高亮的文字==
H<sub>2</sub>O 下标
阿日哥<sup>TM</sup>  上标
X^2^ 上标
H~2~O 下标
```

**这是加粗的文字**
*这是倾斜的文字*`
***这是斜体加粗的文字***
~~这是加删除线的文字~~

==这是高亮的文字==

H<sub>2</sub>O

阿日哥<sup>TM</sup>

X^2^

H~2~O



## 引用

```
>这是引用的内容
>>这是引用的内容
>>>>>>>>>>这是引用的内容
```

>这是引用的内容
>>这是引用的内容
>>
>>>>>>>>>>这是引用的内容



## 分割线

分割线

```
---
---- 
***
*****
```

---
----

***
*****



## 图片

> 插入图片

```
![图片alt](图片地址 ''图片title'')

图片alt就是显示在图片下面的文字，相当于对图片内容的解释。
图片title是图片的标题，当鼠标移到图片上时显示的内容。title可加可不加

![blockchain](https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/
u=702257389,1274025419&fm=27&gp=0.jpg "区块链")

```

![blockchain](https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/
u=702257389,1274025419&fm=27&gp=0.jpg "区块链")



**上传本地图片直接点击导航栏的图片标志，选择图片即可。**



## 超链接

```
[超链接名](超链接地址 "超链接title")
title可加可不加

[简书](http://jianshu.com)
[百度](http://baidu.com)
```

[简书](http://jianshu.com)
[百度](http://baidu.com)



注：Markdown本身语法不支持链接在新页面中打开，貌似简书做了处理，是可以的。别的平台可能就不行了，如果想要在新页面中打开的话可以用html语言的a标签代替。

```
<a href="超链接地址" target="_blank">超链接名</a>

示例
<a href="https://www.jianshu.com/u/1f5ac0cf6a8b" target="_blank">简书</a>
```

<a href="https://www.jianshu.com/u/1f5ac0cf6a8b" target="_blank">简书</a>



## 列表

### 无序列表

语法：
无序列表用 - + * 任何一种都可以

```
- 列表内容
+ 列表内容
* 列表内容

注意：- + * 跟内容之间都要有一个空格
```

- 列表内容
+ 列表内容

* 列表内容

### 有序列表

```
1. 列表内容
2. 列表内容
3. 列表内容

注意：序号跟内容之间要有空格
```

1. 列表内容
2. 列表内容
3. 列表内容

### 列表嵌套

> 上一级和下一级之间敲三个空格即可

上一级和下一级之间敲三个空格即可

- 一级无序列表内容
  - 二级无序列表内容
  - 二级无序列表内容

- 一级无序列表内容
  1. 二级有序列表内容
  2. 二级有序列表内容
  3. 二级有序列表内容

1. 一级有序列表内容
   - 二级无序列表内容
   - 二级无序列表内容
   - 二级无序列表内容
2. 一级有序列表内容
   1. 二级有序列表内容
   2. 二级有序列表内容
   3. 二级有序列表内容



## 表格

> 语法

```
表头|表头|表头
---|:--:|---:
内容|内容|内容
内容|内容|内容

第二行分割表头和内容。
- 有一个就行，为了对齐，多加了几个
文字默认居左
-两边加：表示文字居中
-右边加：表示文字居右
注：原生的语法两边都要用 | 包起来。此处省略
```

> 示例

```
姓名|技能|排行
--|:--:|--:
刘备|哭|大哥
关羽|打|二哥
张飞|骂|三弟
```

| 姓名 | 技能 | 排行 |
| ---- | :--: | ---: |
| 刘备 |  哭  | 大哥 |
| 关羽 |  打  | 二哥 |
| 张飞 |  骂  | 三弟 |



## 代码

>  语法：
> 单行代码：代码之间分别用一个反引号包起来

```
    `代码内容`
```

> 代码块：上下用三个反引号包起来

```
(```注释)
  代码...
  代码...
  代码...
(```)
```

> 示例

*单行代码*

```
create database hero;
```

*代码块*

```
function fun(){
         echo "这是一句非常牛逼的代码";
    }
    fun();
```



## 数学公式

### 行内嵌

> 代码

```
内嵌数学公式$\sum_{i=1}^{10}f(i)\,\,\text{thanks}$
```

内嵌数学公式$\sum_{i=1}^{10}f(i)\,\,\text{thanks}$



### 行间公式

```行间公式代码
$$
\sum_{i=1}^{10}f(i)\,\,\text{thanks}
$$
```



$$
\sum_{i=1}^{10}f(i)\,\,\text{thanks}
$$



### 公式自动编号

- 自动编号的公式可以用如下方法表示：

  `\begin{equation} 数学公式 \label{eq:当前公式名} \end{equation} `

**自动编号后的公式可在全文任意处使用 `\eqref{eq:公式名}` 语句引用。**

- 例子：

```
在公式 \eqref{eq:sample} 中，我们看到了这个被自动编号的公式。
\begin{equation}
E=mc^2 \text{，自动编号公式示例}
\label{eq:Sample}
\end{equation}
```

$$
在公式 \eqref{eq:sample} 中，我们看到了这个被自动编号的公式。
\begin{equation}
E=mc^2 \text{，自动编号公式示例}
\label{eq:Sample}
\end{equation}
$$





### 输入组合数

两种方法：`$\binom{n}{m}$`和`$n\choose m$`

也可以直接输入`C_n^mA_n^m`

效果：
$$
\binom{n}{m}\\
C_n^mA_n^m
$$




### 关于积分的输入

使用 `\int_积分下限^积分上限 {被积表达式}` 来输入一个积分。

例子：

```
$$\int_0^1 {x^2} \,{\rm d}x$$
```

$$\int_0^1 {x^2} \,{\rm d}x$$

本例中 `\,` （加入空格）和 `{\rm d}`（使用罗马字符d部分可省略，但建议加入，能使式子更美观。



### 关于矢量的输入

使用 `\vec{矢量}` 来自动产生一个矢量。也可以使用 `\overrightarrow` 等命令自定义字母上方的符号。

- 例子：

```
$$\vec{a} \cdot \vec{b}=0$$
```

$$\vec{a} \cdot \vec{b}=0$$

- 例子：

```
$$\overleftarrow{xy} \quad and \quad \overleftrightarrow{xy} \quad and \quad \overrightarrow{xy}$$
```

$$\overleftarrow{xy} \quad and \quad \overleftrightarrow{xy} \quad and \quad \overrightarrow{xy}$$



### 关于极限的输入

使用 `\lim_{变量 \to 表达式} 表达式` 来输入一个极限。如有需求，可以更改 `\to` 符号至任意符号。

例子：

```
$$ \lim_{n \to +\infty} \frac{1}{n(n+1)} \quad and \quad \lim_{x\leftarrow{示例}} \frac{1}{n(n+1)} $$
```

显示：

$$ \lim_{n \to +\infty} \frac{1}{n(n+1)} \quad and \quad \lim_{x\leftarrow{示例}} \frac{1}{n(n+1)} $$



### 输入累加累乘运算

使用 `\sum_{下标表达式}^{上标表达式} {累加表达式}` 来输入一个累加。 
与之类似，使用 `\prod` `\bigcup` `\bigcap` 来分别输入累乘、并集和交集。 
此类符号在行内显示时上下标表达式将会移至右上角和右下角。

- 例子：

```
$$\sum_{i=1}^n \frac{1}{i^2} \quad and \quad \prod_{i=1}^n \frac{1}{i^2} \quad and \quad \bigcup_{i=1}^{2} R$$
```

$$\sum_{i=1}^n \frac{1}{i^2} \quad and \quad \prod_{i=1}^n \frac{1}{i^2} \quad and \quad \bigcup_{i=1}^{2} R$$



### 输入省略号

数学公式中常见的省略号有两种，`\ldots` 表示与文本底线对齐的省略号，`\cdots` 表示与文本中线对齐的省略号。

- 例子：

```
$$f(x_1,x_2,\underbrace{\ldots}_{\rm ldots} ,x_n) = x_1^2 + x_2^2 + \underbrace{\cdots}_{\rm cdots} + x_n^2$$
```

$$f(x_1,x_2,\underbrace{\ldots}_{\rm ldots} ,x_n) = x_1^2 + x_2^2 + \underbrace{\cdots}_{\rm cdots} + x_n^2$$



### 输入开方

使用 `\sqrt [根指数，省略时为2] {被开方数}` 命令输入开方。

- 例子：

```
$$\sqrt{2} \quad and \quad \sqrt[n]{3}$$
```

$$\sqrt{2} \quad and \quad \sqrt[n]{3}$$



### 输入分数

通常使用 `\frac {分子} {分母}` 命令产生一个分数，分数可嵌套。 
便捷情况可直接输入 `\frac ab` 来快速生成一个 $\frac ab$。 
如果分式很复杂，亦可使用 `分子 \over 分母` 命令，此时分数仅有一层。

- 例子：

```
$$\frac{a-1}{b-1} \quad and \quad {a+1\over b+1}$$
```

$$\frac{a-1}{b-1} \quad and \quad {a+1\over b+1}$$



### 输入括号和分隔符

`()`、`[]` 和 `|` 表示符号本身，使用 `\{\}` 来表示 `{}` 。当要显示大号的括号或分隔符时，要用 `\left` 和 `\right` 命令。

一些特殊的括号：

|  输入   |   显示    |  输入   |   显示    |
| :-----: | :-------: | :-----: | :-------: |
| \langle | $\langle$ | \rangle | $\rangle$ |
| \lceil  | $\lceil$  | \rceil  | $\rceil$  |
| \lfloor | $\lfloor$ | \rfloor | $\rfloor$ |
| \lbrace | $\lbrace$ | \rbrace | $\rbrace$ |

- 例子：

```
$$ f(x,y,z) = 3y^2z \left( 3+\frac{7x+5}{1+y^2} \right) $$
```

$$ f(x,y,z) = 3y^2z \left( 3+\frac{7x+5}{1+y^2} \right) $$



### 输入上下标

`^` 表示上标, `_` 表示下标。如果上下标的内容多于一个字符，需要用 `{}` 将这些内容括成一个整体。上下标可以嵌套，也可以同时使用。

- 例子：

```
$$ x^{y^z}=(1+{\rm e}^x)^{-2xy^w} $$
```

- 显示：

$$ x^{y^z}=(1+{\rm e}^x)^{-2xy^w} $$



另外，如果要在左右两边都有上下标，可以用 `\sideset` 命令。

- 例子：

```
$$ \sideset{^1_2}{^3_4}\bigotimes $$
```

- 显示：

$$ \sideset{^1_2}{^3_4}\bigotimes $$






## 流程图

```
​```flow
st=>start: 开始
op=>operation: My Operation
cond=>condition: Yes or No?
e=>end
st->op->cond
cond(yes)->e
cond(no)->op
&```
```

```flow
st=>start: 开始
op=>operation: My Operation
cond=>condition: Yes or No?
e=>end
st->op->cond
cond(yes)->e
cond(no)->op
&```
```





## 希腊字母表

|                             字母                             |     代码     |
| :----------------------------------------------------------: | :----------: |
|                              α                               |   $alpha$    |
|                              β                               |    $beta$    |
|                              γ                               |   $gamma$    |
|  ![\Gamma](https://math.jianshu.com/math?formula=%5CGamma)   |   $Gamma$    |
|                              δ                               |   $delta$    |
|  ![\Delta](https://math.jianshu.com/math?formula=%5CDelta)   |   $Delta$    |
| ![\epsilon](https://math.jianshu.com/math?formula=%5Cepsilon) |  $epsilon$   |
|                              ε                               | $varepsilon$ |
|                              ζ                               |    $zeta$    |
|                              η                               |    $eta$     |
|                              θ                               |   $theta$    |
|                              Θ                               |   $Theta$    |
| ![\vartheta](https://math.jianshu.com/math?formula=%5Cvartheta) |  $vartheta$  |
|   ![\iota](https://math.jianshu.com/math?formula=%5Ciota)    |    $iota$    |
|  ![\kappa](https://math.jianshu.com/math?formula=%5Ckappa)   |   $kappa$    |
|                              λ                               |   $lambda$   |
|                              Λ                               |   $Lambda$   |
|                              μ                               |     $mu$     |
|     ![\nu](https://math.jianshu.com/math?formula=%5Cnu)      |     $nu$     |
|     ![\xi](https://math.jianshu.com/math?formula=%5Cxi)      |     $xi$     |
|     ![\Xi](https://math.jianshu.com/math?formula=%5CXi)      |     $Xi$     |
|     ![\pi](https://math.jianshu.com/math?formula=%5Cpi)      |     $pi$     |
|     ![\Pi](https://math.jianshu.com/math?formula=%5CPi)      |     $Pi$     |
|  ![\varpi](https://math.jianshu.com/math?formula=%5Cvarpi)   |   $varpi$    |
|    ![\rho](https://math.jianshu.com/math?formula=%5Crho)     |    $rho$     |
|                              ϱ                               |   $varrho$   |
|  ![\sigma](https://math.jianshu.com/math?formula=%5Csigma)   |   $sigma$    |
|  ![\Sigma](https://math.jianshu.com/math?formula=%5CSigma)   |   $Sigma$    |
|                              ς                               |  $varsigma$  |
|    ![\tau](https://math.jianshu.com/math?formula=%5Ctau)     |    $tau$     |
| ![\upsilon](https://math.jianshu.com/math?formula=%5Cupsilon) |  $upsilon$   |
| ![\Upsilon](https://math.jianshu.com/math?formula=%5CUpsilon) |  $Upsilon$   |
|    ![\phi](https://math.jianshu.com/math?formula=%5Cphi)     |    $phi$     |
|    ![\Phi](https://math.jianshu.com/math?formula=%5CPhi)     |    $Phi$     |
| ![\varphi](https://math.jianshu.com/math?formula=%5Cvarphi)  |   $varphi$   |
|    ![\chi](https://math.jianshu.com/math?formula=%5Cchi)     |    $chi$     |
|    ![\psi](https://math.jianshu.com/math?formula=%5Cpsi)     |    $psi$     |
|    ![\Psi](https://math.jianshu.com/math?formula=%5CPsi)     |    $Psi$     |
|                              Ω                               |   $Omega$    |
|                              ω                               |   $omega$    |

|   输入   |                             显示                             |  输入   |                            显示                             |   输入   |                             显示                             |   输入   |                             显示                             |
| :------: | :----------------------------------------------------------: | :-----: | :---------------------------------------------------------: | :------: | :----------------------------------------------------------: | :------: | :----------------------------------------------------------: |
|  \alpha  |  ![\alpha](https://math.jianshu.com/math?formula=%5Calpha)   |    A    |        ![A](https://math.jianshu.com/math?formula=A)        |  \beta   |   ![\beta](https://math.jianshu.com/math?formula=%5Cbeta)    |    B     |        ![B](https://math.jianshu.com/math?formula=B)         |
|  \gamma  |  ![\gamma](https://math.jianshu.com/math?formula=%5Cgamma)   | \Gamma  |  ![\Gamma](https://math.jianshu.com/math?formula=%5CGamma)  |  \delta  |  ![\delta](https://math.jianshu.com/math?formula=%5Cdelta)   |  \Delta  |  ![\Delta](https://math.jianshu.com/math?formula=%5CDelta)   |
| \epsilon | ![\epsilon](https://math.jianshu.com/math?formula=%5Cepsilon) |    E    |        ![E](https://math.jianshu.com/math?formula=E)        |  \zeta   |   ![\zeta](https://math.jianshu.com/math?formula=%5Czeta)    |    Z     |        ![Z](https://math.jianshu.com/math?formula=Z)         |
|   \eta   |    ![\eta](https://math.jianshu.com/math?formula=%5Ceta)     |    H    |        ![H](https://math.jianshu.com/math?formula=H)        |  \theta  |  ![\theta](https://math.jianshu.com/math?formula=%5Ctheta)   |  \Theta  |  ![\Theta](https://math.jianshu.com/math?formula=%5CTheta)   |
|  \iota   |   ![\iota](https://math.jianshu.com/math?formula=%5Ciota)    |    I    |        ![I](https://math.jianshu.com/math?formula=I)        |  \kappa  |  ![\kappa](https://math.jianshu.com/math?formula=%5Ckappa)   |    K     |        ![K](https://math.jianshu.com/math?formula=K)         |
| \lambda  | ![\lambda](https://math.jianshu.com/math?formula=%5Clambda)  | \Lambda | ![\Lambda](https://math.jianshu.com/math?formula=%5CLambda) |   \mu    |     ![\mu](https://math.jianshu.com/math?formula=%5Cmu)      |    M     |        ![M](https://math.jianshu.com/math?formula=M)         |
|   \nu    |     ![\nu](https://math.jianshu.com/math?formula=%5Cnu)      |    N    |        ![N](https://math.jianshu.com/math?formula=N)        |   \xi    |     ![\xi](https://math.jianshu.com/math?formula=%5Cxi)      |   \Xi    |     ![\Xi](https://math.jianshu.com/math?formula=%5CXi)      |
|    o     |        ![o](https://math.jianshu.com/math?formula=o)         |    O    |        ![O](https://math.jianshu.com/math?formula=O)        |   \pi    |     ![\pi](https://math.jianshu.com/math?formula=%5Cpi)      |   \Pi    |     ![\Pi](https://math.jianshu.com/math?formula=%5CPi)      |
|   \rho   |    ![\rho](https://math.jianshu.com/math?formula=%5Crho)     |    P    |        ![P](https://math.jianshu.com/math?formula=P)        |  \sigma  |  ![\sigma](https://math.jianshu.com/math?formula=%5Csigma)   |  \Sigma  |  ![\Sigma](https://math.jianshu.com/math?formula=%5CSigma)   |
|   \tau   |    ![\tau](https://math.jianshu.com/math?formula=%5Ctau)     |    T    |        ![T](https://math.jianshu.com/math?formula=T)        | \upsilon | ![\upsilon](https://math.jianshu.com/math?formula=%5Cupsilon) | \Upsilon | ![\Upsilon](https://math.jianshu.com/math?formula=%5CUpsilon) |
|   \phi   |    ![\phi](https://math.jianshu.com/math?formula=%5Cphi)     |  \Phi   |    ![\Phi](https://math.jianshu.com/math?formula=%5CPhi)    |   \chi   |    ![\chi](https://math.jianshu.com/math?formula=%5Cchi)     |    X     |        ![X](https://math.jianshu.com/math?formula=X)         |
|   \psi   |    ![\psi](https://math.jianshu.com/math?formula=%5Cpsi)     |  \Psi   |    ![\Psi](https://math.jianshu.com/math?formula=%5CPsi)    |  \omega  |  ![\omega](https://math.jianshu.com/math?formula=%5Comega)   |  \Omega  |  ![\Omega](https://math.jianshu.com/math?formula=%5COmega)   |



**部分字母有变量专用形式，以 `\var-` 开头。**

| 小写形式 | 大写形式 |  变量形式   |                             显示                             |
| :------: | :------: | :---------: | :----------------------------------------------------------: |
| \epsilon |    E     | \varepsilon | ![\epsilon \mid E \mid \varepsilon](https://math.jianshu.com/math?formula=%5Cepsilon%20%5Cmid%20E%20%5Cmid%20%5Cvarepsilon) |
|  \theta  |  \Theta  |  \vartheta  | ![\theta \mid \Theta \mid \vartheta](https://math.jianshu.com/math?formula=%5Ctheta%20%5Cmid%20%5CTheta%20%5Cmid%20%5Cvartheta) |
|   \rho   |    P     |   \varrho   | ![\rho \mid P \mid \varrho](https://math.jianshu.com/math?formula=%5Crho%20%5Cmid%20P%20%5Cmid%20%5Cvarrho) |
|  \sigma  |  \Sigma  |  \varsigma  | ![\sigma \mid \Sigma \mid \varsigma](https://math.jianshu.com/math?formula=%5Csigma%20%5Cmid%20%5CSigma%20%5Cmid%20%5Cvarsigma) |
|   \phi   |   \Phi   |   \varphi   | ![\phi \mid \Phi \mid \varphi](https://math.jianshu.com/math?formula=%5Cphi%20%5Cmid%20%5CPhi%20%5Cmid%20%5Cvarphi) |







## 常见运算符



### 关系运算符

|    输入    |                             显示                             |    输入    |                             显示                             |   输入    |                             显示                             |
| :--------: | :----------------------------------------------------------: | :--------: | :----------------------------------------------------------: | :-------: | :----------------------------------------------------------: |
|    \pm     |     ![\pm](https://math.jianshu.com/math?formula=%5Cpm)      |   \times   |  ![\times](https://math.jianshu.com/math?formula=%5Ctimes)   |   \div    |    ![\div](https://math.jianshu.com/math?formula=%5Cdiv)     |
|   \nmid    |   ![\nmid](https://math.jianshu.com/math?formula=%5Cnmid)    |   \cdot    |   ![\cdot](https://math.jianshu.com/math?formula=%5Ccdot)    |   \circ   |   ![\circ](https://math.jianshu.com/math?formula=%5Ccirc)    |
|  \bigodot  | ![\bigodot](https://math.jianshu.com/math?formula=%5Cbigodot) | \bigotimes | ![\bigotimes](https://math.jianshu.com/math?formula=%5Cbigotimes) | \bigoplus | ![\bigoplus](https://math.jianshu.com/math?formula=%5Cbigoplus) |
|    \geq    |    ![\geq](https://math.jianshu.com/math?formula=%5Cgeq)     |    \neq    |    ![\neq](https://math.jianshu.com/math?formula=%5Cneq)     |  \approx  | ![\approx](https://math.jianshu.com/math?formula=%5Capprox)  |
|    \sum    |    ![\sum](https://math.jianshu.com/math?formula=%5Csum)     |   \prod    |   ![\prod](https://math.jianshu.com/math?formula=%5Cprod)    |  \coprod  | ![\coprod](https://math.jianshu.com/math?formula=%5Ccoprod)  |
|  \propto   |                          $\propto$                           |    \sim    |                            $\sim$                            |  \simeq   |                           $\simeq$                           |
|   \Join    |                           $\Join$                            | \thicksim  |                         $\thicksim$                          | \backsim  |                          $\backsim$                          |
| \backsimeq |                         $\backsimeq$                         |            |                                                              |           |                                                              |



### 集合运算符

|   输入    |                             显示                             |   输入    |                             显示                             |   输入    |                             显示                             |
| :-------: | :----------------------------------------------------------: | :-------: | :----------------------------------------------------------: | :-------: | :----------------------------------------------------------: |
| \emptyset | ![\emptyset](https://math.jianshu.com/math?formula=%5Cemptyset) |    \in    |     ![\in](https://math.jianshu.com/math?formula=%5Cin)      |  \notin   |  ![\notin](https://math.jianshu.com/math?formula=%5Cnotin)   |
|  \subset  | ![\subset](https://math.jianshu.com/math?formula=%5Csubset)  |  \supset  | ![\supset](https://math.jianshu.com/math?formula=%5Csupset)  | \subseteq | ![\subseteq](https://math.jianshu.com/math?formula=%5Csubseteq) |
| \supseteq | ![\supseteq](https://math.jianshu.com/math?formula=%5Csupseteq) |  \bigcap  | ![\bigcap](https://math.jianshu.com/math?formula=%5Cbigcap)  |  \bigcup  | ![\bigcup](https://math.jianshu.com/math?formula=%5Cbigcup)  |
|  \bigvee  | ![\bigvee](https://math.jianshu.com/math?formula=%5Cbigvee)  | \bigwedge | ![\bigwedge](https://math.jianshu.com/math?formula=%5Cbigwedge) | \biguplus | ![\biguplus](https://math.jianshu.com/math?formula=%5Cbiguplus) |



### 对数运算符

| 输入 |                         显示                          | 输入 |                        显示                         | 输入 |                        显示                         |
| :--: | :---------------------------------------------------: | :--: | :-------------------------------------------------: | :--: | :-------------------------------------------------: |
| \log | ![\log](https://math.jianshu.com/math?formula=%5Clog) | \lg  | ![\lg](https://math.jianshu.com/math?formula=%5Clg) | \ln  | ![\ln](https://math.jianshu.com/math?formula=%5Cln) |



### 三角运算符

|   输入   |                             显示                             | 输入 |                         显示                          |   输入   |                             显示                             |
| :------: | :----------------------------------------------------------: | :--: | :---------------------------------------------------: | :------: | :----------------------------------------------------------: |
| 30^\circ | ![30^\circ](https://math.jianshu.com/math?formula=30%5E%5Ccirc) | \bot | ![\bot](https://math.jianshu.com/math?formula=%5Cbot) | \angle A | ![\angle A](https://math.jianshu.com/math?formula=%5Cangle%20A) |
|   \sin   |    ![\sin](https://math.jianshu.com/math?formula=%5Csin)     | \cos | ![\cos](https://math.jianshu.com/math?formula=%5Ccos) |   \tan   |    ![\tan](https://math.jianshu.com/math?formula=%5Ctan)     |
|   \csc   |    ![\csc](https://math.jianshu.com/math?formula=%5Ccsc)     | \sec | ![\sec](https://math.jianshu.com/math?formula=%5Csec) |   \cot   |    ![\cot](https://math.jianshu.com/math?formula=%5Ccot)     |



### 微积分运算符

|  输入   |                            显示                             |  输入  |                           显示                            |  输入  |                           显示                            |
| :-----: | :---------------------------------------------------------: | :----: | :-------------------------------------------------------: | :----: | :-------------------------------------------------------: |
|  \int   |    ![\int](https://math.jianshu.com/math?formula=%5Cint)    | \iint  |  ![\iint](https://math.jianshu.com/math?formula=%5Ciint)  | \iiint | ![\iiint](https://math.jianshu.com/math?formula=%5Ciiint) |
| \iiiint | ![\iiiint](https://math.jianshu.com/math?formula=%5Ciiiint) | \oint  |  ![\oint](https://math.jianshu.com/math?formula=%5Coint)  | \prime | ![\prime](https://math.jianshu.com/math?formula=%5Cprime) |
|  \lim   |    ![\lim](https://math.jianshu.com/math?formula=%5Clim)    | \infty | ![\infty](https://math.jianshu.com/math?formula=%5Cinfty) | \nabla | ![\nabla](https://math.jianshu.com/math?formula=%5Cnabla) |



### 逻辑运算符

|   输入   |                             显示                             |    输入    |                             显示                             |    输入     |                             显示                             |
| :------: | :----------------------------------------------------------: | :--------: | :----------------------------------------------------------: | :---------: | :----------------------------------------------------------: |
| \because | ![\because](https://math.jianshu.com/math?formula=%5Cbecause) | \therefore | ![\therefore](https://math.jianshu.com/math?formula=%5Ctherefore) |   \succeq   |                          $\succeq$                           |
| \forall  | ![\forall](https://math.jianshu.com/math?formula=%5Cforall)  |  \exists   | ![\exists](https://math.jianshu.com/math?formula=%5Cexists)  | \not\subset | ![\not\subset](https://math.jianshu.com/math?formula=%5Cnot%5Csubset) |
|  \not<   |  ![\not<](https://math.jianshu.com/math?formula=%5Cnot%3C)   |   \not>    |  ![\not>](https://math.jianshu.com/math?formula=%5Cnot%3E)   |    \not=    |  ![\not=](https://math.jianshu.com/math?formula=%5Cnot%3D)   |
|  \vdash  |                           $\vdash$                           |   \dashv   |                           $\dashv$                           |   \models   |                          $\models$                           |
|  \prec   |                           $\prec$                            |   \succ    |                           $\succ$                            |   \preceq   |                          $\preceq$                           |
|  \vDash  |                           $\vDash$                           |            |                                                              |             |                                                              |



### 戴帽符号

|    输入    |                             显示                             |      输入       |                             显示                             |
| :--------: | :----------------------------------------------------------: | :-------------: | :----------------------------------------------------------: |
|  \hat{xy}  | ![\hat{xy}](https://math.jianshu.com/math?formula=%5Chat%7Bxy%7D) |  \widehat{xyz}  | ![\widehat{xyz}](https://math.jianshu.com/math?formula=%5Cwidehat%7Bxyz%7D) |
| \tilde{xy} | ![\tilde{xy}](https://math.jianshu.com/math?formula=%5Ctilde%7Bxy%7D) | \widetilde{xyz} | ![\widetilde{xyz}](https://math.jianshu.com/math?formula=%5Cwidetilde%7Bxyz%7D) |
| \check{x}  | ![\check{x}](https://math.jianshu.com/math?formula=%5Ccheck%7Bx%7D) |    \breve{y}    | ![\breve{y}](https://math.jianshu.com/math?formula=%5Cbreve%7By%7D) |
| \grave{x}  | ![\grave{x}](https://math.jianshu.com/math?formula=%5Cgrave%7Bx%7D) |    \acute{y}    | ![\acute{y}](https://math.jianshu.com/math?formula=%5Cacute%7By%7D) |



### 连线符号

|                      输入                      |                             显示                             |
| :--------------------------------------------: | :----------------------------------------------------------: |
|                 \fbox{a+b+c+d}                 | ![\fbox{a+b+c+d}](https://math.jianshu.com/math?formula=%5Cfbox%7Ba%2Bb%2Bc%2Bd%7D) |
|            \overleftarrow{a+b+c+d}             | ![\overleftarrow{a+b+c+d}](https://math.jianshu.com/math?formula=%5Coverleftarrow%7Ba%2Bb%2Bc%2Bd%7D) |
|            \overrightarrow{a+b+c+d}            | ![\overrightarrow{a+b+c+d}](https://math.jianshu.com/math?formula=%5Coverrightarrow%7Ba%2Bb%2Bc%2Bd%7D) |
|          \overleftrightarrow{a+b+c+d}          | ![\overleftrightarrow{a+b+c+d}](https://math.jianshu.com/math?formula=%5Coverleftrightarrow%7Ba%2Bb%2Bc%2Bd%7D) |
|            \underleftarrow{a+b+c+d}            | ![\underleftarrow{a+b+c+d}](https://math.jianshu.com/math?formula=%5Cunderleftarrow%7Ba%2Bb%2Bc%2Bd%7D) |
|           \underrightarrow{a+b+c+d}            | ![\underrightarrow{a+b+c+d}](https://math.jianshu.com/math?formula=%5Cunderrightarrow%7Ba%2Bb%2Bc%2Bd%7D) |
|         \underleftrightarrow{a+b+c+d}          | ![\underleftrightarrow{a+b+c+d}](https://math.jianshu.com/math?formula=%5Cunderleftrightarrow%7Ba%2Bb%2Bc%2Bd%7D) |
|               \overline{a+b+c+d}               | ![\overline{a+b+c+d}](https://math.jianshu.com/math?formula=%5Coverline%7Ba%2Bb%2Bc%2Bd%7D) |
|              \underline{a+b+c+d}               | ![\underline{a+b+c+d}](https://math.jianshu.com/math?formula=%5Cunderline%7Ba%2Bb%2Bc%2Bd%7D) |
|          \overbrace{a+b+c+d}^{Sample}          | ![\overbrace{a+b+c+d}^{Sample}](https://math.jianshu.com/math?formula=%5Coverbrace%7Ba%2Bb%2Bc%2Bd%7D%5E%7BSample%7D) |
|         \underbrace{a+b+c+d}_{Sample}          | ![\underbrace{a+b+c+d}_{Sample}](https://math.jianshu.com/math?formula=%5Cunderbrace%7Ba%2Bb%2Bc%2Bd%7D_%7BSample%7D) |
|  \overbrace{a+\underbrace{b+c}_{1.0}+d}^{2.0}  | ![\overbrace{a+\underbrace{b+c}_{1.0}+d}^{2.0}](https://math.jianshu.com/math?formula=%5Coverbrace%7Ba%2B%5Cunderbrace%7Bb%2Bc%7D_%7B1.0%7D%2Bd%7D%5E%7B2.0%7D) |
| \underbrace{a\cdot a\cdots a}_{b\text{ times}} | ![\underbrace{a\cdot a\cdots a}_{b\text{ times}}](https://math.jianshu.com/math?formula=%5Cunderbrace%7Ba%5Ccdot%20a%5Ccdots%20a%7D_%7Bb%5Ctext%7B%20times%7D%7D) |



### 箭头符号

|   输入   |                             显示                             |  输入   |                            显示                             |    输入    |                             显示                             |
| :------: | :----------------------------------------------------------: | :-----: | :---------------------------------------------------------: | :--------: | :----------------------------------------------------------: |
|   \to    |     ![\to](https://math.jianshu.com/math?formula=%5Cto)      | \mapsto | ![\mapsto](https://math.jianshu.com/math?formula=%5Cmapsto) |            |                                                              |
| \implies | ![\implies](https://math.jianshu.com/math?formula=%5Cimplies) |  \iff   |    ![\iff](https://math.jianshu.com/math?formula=%5Ciff)    | \impliedby | ![\impliedby](https://math.jianshu.com/math?formula=%5Cimpliedby) |

|输入|显示|输入|显示|
|:--:|:--:|:--:|:--:|
|\uparrow|![\uparrow](https://math.jianshu.com/math?formula=%5Cuparrow)|\Uparrow|![\Uparrow](https://math.jianshu.com/math?formula=%5CUparrow)|
|\downarrow|![\downarrow](https://math.jianshu.com/math?formula=%5Cdownarrow)|\Downarrow|![\Downarrow](https://math.jianshu.com/math?formula=%5CDownarrow)|
|\leftarrow|![\leftarrow](https://math.jianshu.com/math?formula=%5Cleftarrow)|\Leftarrow|![\Leftarrow](https://math.jianshu.com/math?formula=%5CLeftarrow)|
|\rightarrow|![\rightarrow](https://math.jianshu.com/math?formula=%5Crightarrow)|\Rightarrow|![\Rightarrow](https://math.jianshu.com/math?formula=%5CRightarrow)|
|\leftrightarrow|![\leftrightarrow](https://math.jianshu.com/math?formula=%5Cleftrightarrow)|\Leftrightarrow|![\Leftrightarrow](https://math.jianshu.com/math?formula=%5CLeftrightarrow)|
|\longleftarrow|![\longleftarrow](https://math.jianshu.com/math?formula=%5Clongleftarrow)|\Longleftarrow|![\Longleftarrow](https://math.jianshu.com/math?formula=%5CLongleftarrow)|
|\longrightarrow|![\longrightarrow](https://math.jianshu.com/math?formula=%5Clongrightarrow)|\Longrightarrow|![\Longrightarrow](https://math.jianshu.com/math?formula=%5CLongrightarrow)|
|\longleftrightarrow|![\longleftrightarrow](https://math.jianshu.com/math?formula=%5Clongleftrightarrow)|\Longleftrightarrow|![\Longleftrightarrow](https://math.jianshu.com/math?formula=%5CLongleftrightarrow)|

- 例子：

  $\neg p\to\phi$



## 字体转换

若要对公式的某一部分字符进行字体转换，可以用 `{\字体 {需转换的部分字符}}` 命令，其中 `\字体` 部分可以参照下表选择合适的字体。一般情况下，公式默认为意大利体 ![italic](https://math.jianshu.com/math?formula=italic) 。

示例中 **全部大写** 的字体仅大写可用。

|输入|说明|显示|输入|说明|显示|
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
|\rm|罗马体|![\rm{Sample}](https://math.jianshu.com/math?formula=%5Crm%7BSample%7D)|\cal|花体|![\cal{SAMPLE}](https://math.jianshu.com/math?formula=%5Ccal%7BSAMPLE%7D)|
|\it|意大利体|![\it{Sample}](https://math.jianshu.com/math?formula=%5Cit%7BSample%7D)|\Bbb|黑板粗体|![\Bbb{SAMPLE}](https://math.jianshu.com/math?formula=%5CBbb%7BSAMPLE%7D)|
|\bf|粗体|![\bf{Sample}](https://math.jianshu.com/math?formula=%5Cbf%7BSample%7D)|\mit|数学斜体|![\mit{SAMPLE}](https://math.jianshu.com/math?formula=%5Cmit%7BSAMPLE%7D)|
|\sf|等线体|![\sf{Sample}](https://math.jianshu.com/math?formula=%5Csf%7BSample%7D)|\scr|手写体|![\scr{SAMPLE}](https://math.jianshu.com/math?formula=%5Cscr%7BSAMPLE%7D)|
|\tt|打字机体|![\tt{Sample}](https://math.jianshu.com/math?formula=%5Ctt%7BSample%7D)|
|\frak|旧德式字体|![\frak{Sample}](https://math.jianshu.com/math?formula=%5Cfrak%7BSample%7D)|

转换字体十分常用，例如在积分中：

- 例子：

```cpp
\begin{array}{cc}
\mathrm{Bad} & \mathrm{Better} \\
\hline \\
\int_0^1 x^2 dx & \int_0^1 x^2 \,{\rm d}x
\end{array}
```

- 显示：
  $$
  \begin{array}{cc}​
  \mathrm{Bad} & \mathrm{Better} \\
  \hline \\
  \int_0^1 x^2 dx & \int_0^1 x^2 \,{\rm d}x
  \end{array}
  $$
  

注意比较两个式子间 ![dx](https://math.jianshu.com/math?formula=dx) 与 ![{\rm d} x](https://math.jianshu.com/math?formula=%7B%5Crm%20d%7D%20x) 的不同。





## 输入矩阵

### 输入无框矩阵

在开头使用 `begin{matrix}`，在结尾使用 `end{matrix}`，在中间插入矩阵元素，每个元素之间插入 `&` ，并在每行结尾处使用 `\\` 。
使用矩阵时必须声明 `$` 或 `$$` 符号。

- 例子：



```ruby
$$
        \begin{matrix}
        1 & x & x^2 \\
        1 & y & y^2 \\
        1 & z & z^2 \\
        \end{matrix}
$$
```

- 显示：
  $$
  \begin{matrix}
          1 & x & x^2 \\
          1 & y & y^2 \\
          1 & z & z^2 \\
          \end{matrix}
  $$



### 输入带边框矩阵

在开头将 `matrix` 替换为 `pmatrix` `bmatrix` `Bmatrix` `vmatrix` `Vmatrix` 。

- 例子：

```ruby
$ \begin{matrix} 1 & 2 \\ 3 & 4 \\ \end{matrix} $
$ \begin{pmatrix} 1 & 2 \\ 3 & 4 \\ \end{pmatrix} $
$ \begin{bmatrix} 1 & 2 \\ 3 & 4 \\ \end{bmatrix} $
$ \begin{Bmatrix} 1 & 2 \\ 3 & 4 \\ \end{Bmatrix} $
$ \begin{vmatrix} 1 & 2 \\ 3 & 4 \\ \end{vmatrix} $
$ \begin{Vmatrix} 1 & 2 \\ 3 & 4 \\ \end{Vmatrix} $
```

$ \begin{matrix} 1 & 2 \\ 3 & 4 \\ \end{matrix} $

$ \begin{pmatrix} 1 & 2 \\ 3 & 4 \\ \end{pmatrix} $

$ \begin{bmatrix} 1 & 2 \\ 3 & 4 \\ \end{bmatrix} $

$ \begin{Bmatrix} 1 & 2 \\ 3 & 4 \\ \end{Bmatrix} $

$ \begin{vmatrix} 1 & 2 \\ 3 & 4 \\ \end{vmatrix} $

$ \begin{Vmatrix} 1 & 2 \\ 3 & 4 \\ \end{Vmatrix} $



### 输入带省略符号的矩阵

使用 `\cdots` ![\cdots](https://math.jianshu.com/math?formula=%5Ccdots) , `\ddots` ![\ddots](https://math.jianshu.com/math?formula=%5Cddots) , `\vdots` ![\vdots](https://math.jianshu.com/math?formula=%5Cvdots) 来输入省略符号。

- 例子：

```ruby
$$
        \begin{pmatrix}
        1 & a_1 & a_1^2 & \cdots & a_1^n \\
        1 & a_2 & a_2^2 & \cdots & a_2^n \\
        \vdots & \vdots & \vdots & \ddots & \vdots \\
        1 & a_m & a_m^2 & \cdots & a_m^n \\
        \end{pmatrix}
$$
```


$$
\begin{pmatrix}
        1 & a_1 & a_1^2 & \cdots & a_1^n \\
        1 & a_2 & a_2^2 & \cdots & a_2^n \\
        \vdots & \vdots & \vdots & \ddots & \vdots \\
        1 & a_m & a_m^2 & \cdots & a_m^n \\
        \end{pmatrix}
$$


### 输入带分割符号的矩阵

- 例子：

```ruby
$$
\left[
    \begin{array}{cc|c}
      1&2&3\\
      4&5&6
    \end{array}
\right]
$$
```

$$
\left[
    \begin{array}{cc|c}
      1&2&3\\
      4&5&6
    \end{array}
\right]
$$

其中 `cc|c` 代表在一个三列矩阵中的第二和第三列之间插入分割线。



### 输入行中矩阵

若想在一行内显示矩阵，
使用`\bigl(\begin{smallmatrix} ... \end{smallmatrix}\bigr)`。

- 例子：

- ```ruby
  这是一个行中矩阵的示例 $\bigl( \begin{smallmatrix} a & b \\ c & d \end{smallmatrix} \bigr)$ 。
  ```

显示：$\bigl( \begin{smallmatrix} a & b \\ c & d \end{smallmatrix} \bigr)$



## 方程式序列

### 输入方程式序列并且对齐

人们经常想要一列整齐且居中的方程式序列。使用 `\begin{align}…\end{align}` 来创造一列方程式，其中在每行结尾处使用 `\\` 。
使用方程式序列无需声明公式符号 `$` 或 `$$` 。

请注意 `{align}` 语句是 **自动编号** 的。

```cpp
\begin{align}
\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
 & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\ 
 & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\
 & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\ 
 & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
\end{align}
```

$$
\begin{align}
\sqrt{37} & = \sqrt{\frac{73^2-1}{12^2}} \\
 & = \sqrt{\frac{73^2}{12^2}\cdot\frac{73^2-1}{73^2}} \\ 
 & = \sqrt{\frac{73^2}{12^2}}\sqrt{\frac{73^2-1}{73^2}} \\
 & = \frac{73}{12}\sqrt{1 - \frac{1}{73^2}} \\ 
 & \approx \frac{73}{12}\left(1 - \frac{1}{2\cdot73^2}\right)
\end{align}
$$



### 在方程式序列中表达原因

在 `{align}` 中灵活组合 `\text` 和 `\tag` 语句。`\tag` 语句编号优先级高于自动编号。

- 例子：

```ruby
\begin{align}
   v + w & = 0  &\text{Given} \tag 1\\
   -w & = -w + 0 & \text{additive identity} \tag 2\\
   -w + 0 & = -w + (v + w) & \text{equations $(1)$ and $(2)$}
\end{align}
```

$$
\begin{align}
   v + w & = 0  &\text{Given} \tag 1\\
   -w & = -w + 0 & \text{additive identity} \tag 2\\
   -w + 0 & = -w + (v + w) & \text{equations $(1)$ and $(2)$}
\end{align}
$$

本例中第一、第二行的自动编号被 `\tag` 语句覆盖，第三行的编号为自动编号



### 大括号和行标的使用

使用 `\left` 和 `\right` 来创建自动匹配高度的 (圆括号)，[方括号] 和 {花括号} 。 
在每个公式末尾前使用 `\tag{行标}` 来实现行标。

- 例子：

```
$$
f\left(
   \left[ 
     \frac{
       1+\left\{x,y\right\}
     }{
       \left(
          \frac{x}{y}+\frac{y}{x}
       \right)
       \left(u+1\right)
     }+a
   \right]^{3/2}
\right)
\tag{行标}
$$
```

$$
f\left(
   \left[ 
     \frac{
       1+\left\{x,y\right\}
     }{
       \left(
          \frac{x}{y}+\frac{y}{x}
       \right)
       \left(u+1\right)
     }+a
   \right]^{3/2}
\right)
\tag{行标}
$$

如果你需要在不同的行显示对应括号，可以在每一行对应处使用 `\left.` 或 `\right.` 来放一个"影子"括号：

- 例子：

```
$$
\begin{aligned}
a=&\left(1+2+3+  \cdots \right. \\
& \cdots+ \left. \infty-2+\infty-1+\infty\right)
\end{aligned}
$$
```

- 显示： 

- $$
  \begin{aligned}
  a=&\left(1+2+3+  \cdots \right. \\
  & \cdots+ \left. \infty-2+\infty-1+\infty\right)
  \end{aligned}
  $$



### 添加注释文字

在 `\text {文字}` 中仍可以使用 `$公式$` 插入其它公式。

- 例子：

```
$$
f(n)= \begin{cases} n/2, & \text {if $n$ is even} \\ 3n+1, & \text{if $n$ is odd} \end{cases}
$$
```

- 显示： 
  $$
  f(n)= \begin{cases} n/2, & \text {if $n$ is even} \\ 3n+1, & \text{if $n$ is odd} \end{cases}
  $$



### 在字符间加入空格

有四种宽度的空格可以使用： `\,`、`\;`、`\quad` 和 `\qquad` 。

- 例子：

```
$$ a \, b \mid a \; b \mid a \quad b \mid a \qquad b $$
```

- 显示：

$$ a \, b \mid a \; b \mid a \quad b \mid a \qquad b $$

当然，使用 `\text {n个空格}` 也可以达到同样效果。

## 条件表达式

### 输入条件表达式

使用 `begin{cases}` 来创造一组条件表达式，在每一行条件中插入 `&` 来指定需要对齐的内容，并在每一行结尾处使用 `\\`，以 `end{cases}` 结束。
条件表达式无需声明 `$` 或 `$$` 符号。

- 例子：

```ruby
$$
        f(n) =
        \begin{cases}
        n/2,  & \text{if $n$ is even} \\
        3n+1, & \text{if $n$ is odd}
        \end{cases}
$$
```

$$
f(n) =
        \begin{cases}
        n/2,  & \text{if $n$ is even} \\
        3n+1, & \text{if $n$ is odd}
        \end{cases}
$$



### 输入左侧对其的条件表达式

若想让文字在 **左侧对齐显示** ，则有如下方式：

- 例子：

```ruby
$$
        \left.
        \begin{array}{l}
        \text{if $n$ is even:}&n/2\\
        \text{if $n$ is odd:}&3n+1
        \end{array}
        \right\}
        =f(n)
$$
```

$$
\left.
        \begin{array}{l}
        \text{if $n$ is even:}&n/2\\
        \text{if $n$ is odd:}&3n+1
        \end{array}
        \right\}
        =f(n)
$$



### 表达式适应行高

在一些情况下，条件表达式中某些行的行高为非标准高度，此时使用 `\\[2ex]` 语句代替该行末尾的 `\\` 来让编辑器适配。

- 例子：

  **不适配[2ex]**

```ruby
$$
f(n) = 
\begin{cases}
\frac{n}{2},  & \text{if $n$ is even} \\
3n+1, & \text{if $n$ is odd}
\end{cases}
$$
```

$$
f(n) = 
\begin{cases}
\frac{n}{2},  & \text{if $n$ is even} \\
3n+1, & \text{if $n$ is odd}
\end{cases}
$$

​		**适配[2ex]**

```ruby
$$
f(n) = 
\begin{cases}
\frac{n}{2},  & \text{if $n$ is even} \\[2ex]
3n+1, & \text{if $n$ is odd}
\end{cases}
$$
```

$$
f(n) = 
\begin{cases}
\frac{n}{2},  & \text{if $n$ is even} \\[2ex]
3n+1, & \text{if $n$ is odd}
\end{cases}
$$

**一个 `[ex]` 指一个 "X-Height"，即x字母高度。可以根据情况指定多个 `[ex]`，如 `[3ex]`、`[4ex]` 等。**
其实可以在任何地方使用 `\\[2ex]` 语句，只要你觉得合适。



## 数组或表格

### 输入一个数组或表格

通常，一个格式化后的表格比单纯的文字或排版后的文字更具有可读性。数组和表格均以 `begin{array}` 开头，并在其后定义列数及每一列的文本对齐属性，`c` `l` `r` 分别代表居中、左对齐及右对齐。若需要插入垂直分割线，在定义式中插入 `|` ，若要插入水平分割线，在下一行输入前插入 `\hline` 。与矩阵相似，每行元素间均须要插入 `&` ，每行元素以 `\\` 结尾，最后以 `end{array}` 结束数组。
使用单个数组或表格时无需声明 `$` 或 `$$` 符号。

- 例子：

```cpp
\begin{array}{c|lcr}
n & \text{左对齐} & \text{居中对齐} & \text{右对齐} \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i
\end{array}
```

$$
\begin{array}{c|lcr}
n & \text{左对齐} & \text{居中对齐} & \text{右对齐} \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i
\end{array}
$$



### 输入嵌套表格或数组

多个数组/表格可 **互相嵌套** 并组成一组数组/一组表格。
使用嵌套前必须声明 `$$` 符号。

- 例子：

```cpp
$$
% outer vertical array of arrays 外层垂直表格
\begin{array}{c}
    % inner horizontal array of arrays 内层水平表格
    \begin{array}{cc}
        % inner array of minimum values 内层"最小值"数组
        \begin{array}{c|cccc}
        \text{min} & 0 & 1 & 2 & 3\\
        \hline
        0 & 0 & 0 & 0 & 0\\
        1 & 0 & 1 & 1 & 1\\
        2 & 0 & 1 & 2 & 2\\
        3 & 0 & 1 & 2 & 3
        \end{array}
    &
        % inner array of maximum values 内层"最大值"数组
        \begin{array}{c|cccc}
        \text{max}&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 1 & 2 & 3\\
        2 & 2 & 2 & 2 & 3\\
        3 & 3 & 3 & 3 & 3
        \end{array}
    \end{array}
    % 内层第一行表格组结束
    \\
    % inner array of delta values 内层第二行Delta值数组
        \begin{array}{c|cccc}
        \Delta&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 0 & 1 & 2\\
        2 & 2 & 1 & 0 & 1\\
        3 & 3 & 2 & 1 & 0
        \end{array}
        % 内层第二行表格组结束
\end{array}
$$
```

$$
% outer vertical array of arrays 外层垂直表格
\begin{array}{c}
    % inner horizontal array of arrays 内层水平表格
    \begin{array}{cc}
        % inner array of minimum values 内层"最小值"数组
        \begin{array}{c|cccc}
        \text{min} & 0 & 1 & 2 & 3\\
        \hline
        0 & 0 & 0 & 0 & 0\\
        1 & 0 & 1 & 1 & 1\\
        2 & 0 & 1 & 2 & 2\\
        3 & 0 & 1 & 2 & 3
        \end{array}
    &
        % inner array of maximum values 内层"最大值"数组
        \begin{array}{c|cccc}
        \text{max}&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 1 & 2 & 3\\
        2 & 2 & 2 & 2 & 3\\
        3 & 3 & 3 & 3 & 3
        \end{array}
    \end{array}
    % 内层第一行表格组结束
    \\
    % inner array of delta values 内层第二行Delta值数组
        \begin{array}{c|cccc}
        \Delta&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 0 & 1 & 2\\
        2 & 2 & 1 & 0 & 1\\
        3 & 3 & 2 & 1 & 0
        \end{array}
        % 内层第二行表格组结束
\end{array}
$$

$$
% outer vertical array of arrays 外层垂直表格
\begin{array}{c}
    % inner horizontal array of arrays 内层水平表格
    \begin{array}{cc}
        % inner array of minimum values 内层"最小值"数组
        \begin{array}{c|cccc}
        \text{min} & 0 & 1 & 2 & 3\\
        \hline
        0 & 0 & 0 & 0 & 0\\
        1 & 0 & 1 & 1 & 1\\
        2 & 0 & 1 & 2 & 2\\
        3 & 0 & 1 & 2 & 3
        \end{array}
    &
        % inner array of maximum values 内层"最大值"数组
        \begin{array}{c|cccc}
        \text{max}&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 1 & 2 & 3\\
        2 & 2 & 2 & 2 & 3\\
        3 & 3 & 3 & 3 & 3
        \end{array}
    \end{array}
    % 内层第一行表格组结束
    \\
    % inner array of delta values 内层第二行Delta值数组
        \begin{array}{c|cccc}
        \Delta&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 0 & 1 & 2\\
        2 & 2 & 1 & 0 & 1\\
        3 & 3 & 2 & 1 & 0
        \end{array}
        % 内层第二行表格组结束
\end{array}
$$

### 输入方程组

使用 `\begin{array}…\end{array}` 和 `\left\{…\right.` 来创建一个方程组。

- 例子：



```ruby
$$
\left\{ 
\begin{array}{c}
a_1x+b_1y+c_1z=d_1 \\ 
a_2x+b_2y+c_2z=d_2 \\ 
a_3x+b_3y+c_3z=d_3
\end{array}
\right. 
$$
```

$$
\left\{ 
\begin{array}{c}
a_1x+b_1y+c_1z=d_1 \\ 
a_2x+b_2y+c_2z=d_2 \\ 
a_3x+b_3y+c_3z=d_3
\end{array}
\right.
$$

或者使用条件表达式组 `\begin{cases}…\end{cases}` 来实现相同效果：



## 连分式

就像输入分式时使用 `\frac` 一样，使用 `\cfrac` 来创建一个连分数。

- 例子：



```ruby
$$
x = a_0 + \cfrac{1^2}{a_1
          + \cfrac{2^2}{a_2
          + \cfrac{3^2}{a_3 + \cfrac{4^4}{a_4 + \cdots}}}}
$$
```

$$
x = a_0 + \cfrac{1^2}{a_1
          + \cfrac{2^2}{a_2
          + \cfrac{3^2}{a_3 + \cfrac{4^4}{a_4 + \cdots}}}}
$$

当然，你可以使用 `\frac` 来表达连分数的 **紧缩记法** 。

- 例子：



```ruby
$$
x = a_0 + \frac{1^2}{a_1+}
          \frac{2^2}{a_2+}
          \frac{3^2}{a_3 +} \frac{4^4}{a_4 +} \cdots
$$
```

$$
x = a_0 + \frac{1^2}{a_1+}
          \frac{2^2}{a_2+}
          \frac{3^2}{a_3 +} \frac{4^4}{a_4 +} \cdots
$$

连分数通常都太大以至于不易排版，所以建议在连分数前后声明 `$$` 符号，或使用像 `[a0;a1,a2,a3,…]` 一样的紧缩记法。



## 交换图表

使用一行 `$ \require{AMScd} $` 语句来允许交换图表的显示。
声明交换图表后，语法与矩阵相似，在开头使用 `begin{CD}`，在结尾使用 `end{CD}`，在中间插入图表元素，每个元素之间插入 `&` ，并在每行结尾处使用 `\\` 。

- 例子：

```ruby
$$
\require{AMScd}
\begin{CD}
    A @>a>> B\\
    @V b V V\# @VV c V\\
    C @>>d> D
\end{CD}
$$
```

$$
\require{AMScd}
\begin{CD}
    A @>a>> B\\
    @V b V V\# @VV c V\\
    C @>>d> D
\end{CD}
$$

其中，`@>>>` 代表右箭头、`@<<<` 代表左箭头、`@VVV` 代表下箭头、`@AAA` 代表上箭头、`@=` 代表水平双实线、`@|` 代表竖直双实线、`@.`代表没有箭头。
在 `@>>>` 的 `>>>` 之间任意插入文字即代表该箭头的注释文字。

- 例子：

```ruby
\begin{CD}
    A @>>> B @>{\text{very long label}}>> C \\
    @. @AAA @| \\
    D @= E @<<< F
\end{CD}
```

$$
\begin{CD}
    A @>>> B @>{\text{very long label}}>> C \\
    @. @AAA @| \\
    D @= E @<<< F
\end{CD}
$$

在本例中， "very long label"自动延长了它所在箭头以及对应箭头的长度。

