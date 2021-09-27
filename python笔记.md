# aletolia-python
introduction to computation and programing using python
## CHAPTER 1 GETTING START
1.计算机可以做些什么？

事实上，计算机只执行了两项工作，一是计算，二是储存计算结果。

此外，我们也可以把知识分成两类

一是陈述性知识（declarative knowledge），它由一些事实性的陈述构成，比如说1+4=5，诸如此类，但我们并不hi因此知道1+4是为什么等于5的。他只是阐述了何为事实

二是命令性的知识，举例来说，下面有一个计算平方根的方法
1. Start with a guess, g.
2. If g*g is close enough to x, stop and say that g is the answer.
3. Otherwise create a new guess by averaging g and x/g, i.e., (g + x/g)/2.
4. Using this new guess, which we again call g, repeat the process until g*g is close
enough to x.
Consider, for example, finding the square root of 25.
1. Set g to some arbitrary value, e.g., 3.
2. We decide that 3*3 = 9 is not close enough to 25.
3. Set g to (3 + 25/3)/2 = 5.67.3
4. We decide that 5.67*5.67 = 32.15 is still not close enough to 25.
5. Set g to (5.67 + 25/5.67)/2 = 5.04
6. We decide that 5.04*5.04 = 25.4 is close enough, so we stop and declare 5.04 to
be an adequate approximation to the square root of 25.
它以一些列的简单的步骤指定了我们在每一步应该做的事，这被称为算法（algorithm）

图灵理论：

丘奇图灵理论直接引出图灵完备性的概念。

如果一种编程语言可以用来模拟通用图灵机，那么它就是图灵完备的。所有现代编程语言都是图灵完备的。因此，任何可以用一种编程语言（如Python）编程的东西都可以用任何其他编程语言（如Java）编程。当然，有些东西可能更容易用一种特定的语言编程，但所有的语言在计算能力方面基本上是平等的。

幸运的是，没有程序员必须用图灵的原始指令构建程序。相反，现代编程语言提供了更大、更方便的原语集。然而，编程作为一系列操作的组装过程的基本思想仍然是核心。

不管一个人有什么样的原语集，也不管他有什么使用它们的方法，编程的优点和缺点都是一样的：计算机会完全按照你的命令去做。这是一件好事，因为这意味着你可以让它做各种有趣和有用的事情。这是一件坏事，因为当它不做你想做的事情时，你通常没有人可以责怪，除了你自己。

世界上有数百种编程语言。没有最好的语言（尽管可以提名一些最差的候选人）。对于不同类型的应用程序，不同的语言是好是坏。例如，MATLAB是处理向量和矩阵的好语言。C语言是编写控制数据网络程序的好语言。PHP是构建网站的好语言。Python是一种很好的通用语言。

每种编程语言都有一组基本结构、语法、静态语义和语义（Each programming language has a set of primitive constructs, a syntax, a static semantics, and a semantics)静态语义定义了哪些句子是有意义的，而语义定义了那些句子的意义。Python中的基本构造包括文本（例如，数字3.2和字符串'abc'）和中缀运算符（例如，+和/）。

一种语言的语法定义了哪些字符串和符号是格式正确的。例如，在英语中，字符串“Cat dog boy.”在语法上是无效的，因为英语的语法不接受形式为<noun><noun>的句子。在Python中，原语序列3.2+3.2在语法上是良好的，但序列3.2和3.2则不是。

静态语义定义了哪些语法上有效的字符串有意义。

例如，在英语中，字符串“I runs fast”的形式是<degen><verb><副词>，这在句法上是可以接受的。然而，它不是有效的英语，因为名词“I”是单数，动词“runs”是复数。这是一个静态语义错误的例子。在Python中，序列3.2/'abc'在语法上是格式良好的（<literal><operator><literal>），但会产生一个静态语义错误，因为将一个数字除以一个字符串是没有意义的。

一种语言的语义将一个意义与没有静态语义错误的每一个语法正确的符号串相关联。在自然语言中，句子的语义可能是模糊的。例如，一句话“I can't prise that student too highly”，可以是奉承或讽刺。但编程语言的设计使得每个合乎规则的程序都有一个确切的含义。

虽然语法错误是最常见的一种错误（特别是对于那些学习新编程语言的人来说），但它们是最不危险的一种错误。每一种严肃的编程语言都能完成检测语法错误的工作，并且不允许用户执行一个有一个语法错误的程序。此外，在大多数情况下，语言系统对错误的位置给出了足够明确的指示，即显然需要做些什么来纠正错误

静态语义错误的情况要复杂一些。

一些编程语言，例如Java，在允许程序执行之前会进行大量的静态语义检查。其他的，例如C和Python（alas），在程序执行之前，进行的静态语义检查相对较少。Python在运行程序时会进行大量的语义检查。

人们通常不会说程序有语义错误。如果一个程序没有语法错误和静态语义错误，它就有一个意义，即它有语义。当然，一个程序语句有语义不代表它有编程者所想要的语义

### CHAPTER 2 INTRODUCTION TO PYTHON

  Python是一种通用编程语言，可以有效地用来构建几乎任何不需要直接访问计算机硬件的程序。Python对于具有高可靠性约束（由于其弱静态语义检查）或由许多人或经过长时间构建和维护（同样由于弱静态语义检查）的程序不是最优的。 然而，与许多其他语言相比，Python确实有一些优势。这是一门相对简单的语言，很容易学。因为Python是被设计来解释的，所以它可以提供对新手程序员特别有用的运行时反馈。还有大量免费提供的库与Python接口并提供有用的扩展功能。

## 2.1THE BASIC ELEMENTS OF PYTHON

Python程序（有时称为脚本）是一系列定义和命令。这些定义由Python解释器在shell中执行。通常，每当程序开始执行时，就会创建一个新的shell。通常一个窗口与shell相关联。
命令，通常称为语句，指示解释器做某事。
    
例如，语句print（'Yankees rule！'）指示解释器调用function print，它将输出字符串Yankees rule！在shell关联的窗口

## 2.1.1 Objects, Expressions, and Numerical Types

对象（object）是Python程序操作的核心内容。每个对象都有一个类型，它定义了程序可以对该对象执行的各种操作。类型可以是标量类型，也可以是非标量类型。标量对象是不可分割的。把它们看作语言的原子。非标量对象，例如字符串，具有内部结构

许多类型的对象可以用程序文本中的文字来表示。例如，文本2是一个表示数字的文本，“abc”是一个表示字符串的文本

Python有四种类型的标量对象：

•int用于表示整数。int类型的文本是以我们通常表示整数的方式编写的（例如，-3、5或10002）。

•float用于表示实数。float类型的文本总是包含一个小数点（例如，3.0或3.17或-28.72）(也可以使用科学记数法编写float类型的文本。例如，literal 1.6E3代表1.6*103，也就是说，它与1600.0相同。）你可能想知道为什么这种类型不称为real。在计算机中，float类型的值作为浮点数存储在计算机中。所有现代编程语言都使用这种表示法，它有许多优点。但是，在某些情况下，它会导致浮点运算的行为方式与实数运算略有不同。我们将在第3.4节中对此进行讨论。

•bool用于表示布尔值True和False。

•none是具有单个值的类型。我们将在第4.1节中对此进行详细说明。

对象和运算符可以组合成表达式，每个表达式的计算结果都是某种类型的对象。我们将其称为表达式的值。

例如，表达式3+2表示int类型的对象5，表达式3.0+2.0表示float类型的对象5.0。

==运算符用于测试两个表达式的计算结果是否相同，以及！=运算符用于测试两个表达式的值是否不同。单个=意味着完全不同的东西，我们将在第2.1.2节中看到。事先警告一下，当你想键入“=”时，你会犯键入“=”的错误。注意这个错误。

符号>>>是一个shell提示符，表示解释器希望用户在shell中键入一些Python代码。当解释器计算在提示符处输入的Python代码时，会生成带有提示符的行下方的行，如以下与解释器的交互所示：

>>> 3 + 2

5

>>> 3.0 + 2.0

5.0

>>> 3 != 2

True

内置的Python函数type可用于查找对象的类型：

>>> type(3)

<type 'int'>

>>> type(3.0)

<type 'float'>

i+j是i和j的和。如果i和j都是int类型，则结果是int。如果其中任何一个是float，则结果是float。

i–j是i减去j。如果i和j都是int类型，则结果是int。如果其中任何一个是float，则结果是float。

i*j是i和j的乘积。如果i和j都是int类型，则结果是int。如果其中任何一个是浮点数，则结果是浮点数。

i//j是整数除法。例如，6//2的值是int 3，6//4的值是int 1。该值为1，因为整数除法返回商并忽略余数。如果j==0，则发生错误。

i/j是i除以j。在python3中，/运算符执行浮点除法。
例如，6/4的值为1.5。如果j==0，则发生错误(在Python 2中，当i和j都是int类型时，/运算符的行为方式与//相同，并返回一个int。如果i或j是浮点数，则其行为方式与Python 3/运算符类似。）

i%j是int i除以int j时的余数。它通常发音为“i mod j”，是“i modulo j”的缩写。

i**j是i的j次幂。如果i和j都是int类型，则结果是int。如果其中任何一个是float，则结果是float。

比较运算符为==（相等），！=(不相等）、>（较大）、>=（至少）、<、（较小）和<=（最多）。

bool类型上的基本运算符是and、or和not：

• a and b is True if both a and b are True, and False otherwise.

• a or b is True if at least one of a or b is True, and False otherwise.

• not a is True if a is False, and False if a is True.

### 2.1.2 Variables and Assignment（变量和赋值）

变量提供了一种将名称与对象关联的方法。考虑以下代码

pi = 3

radius = 11

area = pi * (radius**2)

radius = 14

这个程序首先为变量pi与变量radius赋值，并定义其类型为int，接着定义类型为int的第三个变量area
如下图所示

![image](https://user-images.githubusercontent.com/83487754/117415259-b1c74780-af4a-11eb-8868-c715f464e5d4.png)

如果程序执行radius=14，名称radius将返回到int类型的另一个对象，如图2.2的右面板所示。请注意，此赋值对area绑定到的值没有影响。它仍然绑定到表达式3*（11**2）所表示的值。

![image](https://user-images.githubusercontent.com/83487754/117415307-bf7ccd00-af4a-11eb-9efd-05296bab0c85.png)

在Python中，变量只是一个名称，仅此而已。记住这一点，这很重要。赋值语句将=符号左侧的名称与=右侧的表达式表示的对象相关联。记住这个。一个对象可以有一个、多个或没有与之关联的名称。

也许我们不应该说，“变量只是一个名字。”编程语言让我们以一种允许机器执行计算的方式来描述计算。这并不意味着只有计算机才能读取程序。

正如您很快就会发现的，要编写正确工作的程序并不总是那么容易。有经验的程序员会确认，他们花了大量时间阅读程序，试图理解为什么他们会这样做。

因此，以易于阅读的方式编写程序至关重要。变量名的恰当选择对提高可读性起着重要作用在

Python中，变量名可以包含大小写字母、数字（但不能以数字开头）和特殊字符。Python变量名区分大小写，例如Julie和Julie是不同的名称。最后，Python中有少量保留字（有时称为关键字）具有内置含义，不能用作变量名。不同版本的Python的保留字列表略有不同。python3中的保留字是and、as、assert、break、class、continue、def、del、elif、else、except、False、finally、for、from、global、if、import、in、is、lambda、nonlocal、None、not、or、pass、raise、return、True、try、while、with和yield。

 增强代码可读性的另一个好方法是添加注释。 Python不解释符号#后面的文本。

 Python允许多重赋值。声明

 <!--代码1-->

 x, y = 2, 3

 将x绑定到2，y绑定到3。在更改任何绑定之前，将计算赋值右侧的所有表达式。这很方便，因为它允许您使用多重赋值来交换两个变量的绑定。

 ### 2.1.3 Python IDE’s

 直接在shell中键入程序非常不方便。大多数程序员更喜欢使用某种文本编辑器，它是集成开发环境（IDE）的一部分

 一个IDE是标准Python安装包的一部分。

随着Python的普及，其他IDE也如雨后春笋般涌现。这些较新的IDE通常包含一些更流行的Python库，并提供IDLE不提供的功能。Anaconda and Canopy是这些IDE中比较流行的。本书中出现的代码是使用Anaconda创建和测试的。

IDE是应用程序，就像计算机上的任何其他应用程序一样。

所有的Python IDE都提供了

•一个具有语法高亮显示、自动完成和智能缩进的文本编辑器，

•一个具有语法高亮显示的shell

•一个集成的调试器

当IDE启动时，它将打开一个shell窗口，可以在其中键入Python命令。它还将为您提供一个文件菜单和一个编辑菜单（以及一些其他菜单，使您可以方便地做一些事情，如打印您的程序）。

“文件”菜单包含以下命令：

•创建一个新的编辑窗口，您可以在其中键入Python程序，

•打开一个包含现有Python程序的文件，

•将当前编辑窗口的内容保存到一个文件中（文件扩展名为.py）。

“编辑”菜单包括标准文本编辑命令（例如，复制、粘贴和查找）以及一些专门设计的命令，以便于编辑Python代码（例如，缩进区域和注释区域）。

### 2.2 Branching Programs

到目前为止，我们一直在研究的计算类型被称为直线程序。它们按照出现的顺序一个接一个地执行语句，当语句用完时停止。我们可以用直线程序来描述的计算类型不是很有趣。事实上，他们是彻头彻尾的无聊。分支程序更有趣。最简单的分支语句是条件语句。如图2.3的方框部分所示，条件语句有三个部分

•测试，即计算结果为真或假的表达式

•如果测试结果为真，则执行的代码块

•如果测试结果为False，则执行的可选代码块

执行条件语句后，在该语句后面的代码处继续执行


在Python中，条件语句的形式如下

<!--代码2-->
```python
if Boolean expression:
block of code
else:
block of code
or
if Boolean expression:
block of code
```

![image](https://user-images.githubusercontent.com/83487754/117418492-11732200-af4e-11eb-97c5-89d8c764822b.png)

在描述Python语句的形式时，我们使用斜体来描述程序中可能出现的代码类型。例如，boolean exprssion表示任何计算结果为True或False的表达式都可以跟在保留字if后面，而block of code表示任何Python语句序列都可以跟在后面else:.

考虑下面的程序，如果变量x的值是偶数，则打印“偶数”，否则打印“奇数”

<!--代码3-->
```python
if x%2 == 0:
print('Even')
else:
print('Odd')
print('Done with conditional')
```

当x的余数除以2为0时，表达式x%2==0的计算结果为True，否则为False。记住==用于比较，因为=是为赋值保留的

Indentation(缩进）

缩进在Python中具有语义意义。例如，如果上面代码中的最后一条语句缩进，它将是与else关联的一块代码，而非与条件语句关联

Python以这种方式使用缩进是不寻常的。大多数其他编程语言使用某种括号符号来描述代码块，例如，C将块括在括号中{}。

当条件语句的true块或false块包含另一个条件语句时，条件语句被称为嵌套语句。在下面的代码中，最上层if语句的两个分支中都有嵌套条件。

<!--代码3-->
```python
if x%2 == 0:
    if x%3 == 0:
        print('Divisible by 2 and 3')
    else:
        print('Divisible by 2 and not by 3')
elif x%3 == 0:
    print('Divisible by 3 and not by 2')
```

上面代码中的elif代表“else if”，在条件的测试中使用复合布尔表达式通常很方便，例如，

<!--代码4-->
```python
if x < y and x < z:
    print('x is least')
elif y < z:
    print('y is least')
else:
    print('z is least')
```

逻辑判断允许我们编写比直线程序更有趣的程序，但是分支程序的种类仍然非常有限。判断一类程序的能力大小的一种方法是根据它们可以运行的时间长短。假设每行代码需要一个时间单位来执行，那么如果一个直线程序有n行代码，它将需要n个时间单位来运行。有n行代码的分支程序呢？它可能需要不到n个时间单位来运行，但不会超过n个时间单位，因为每行代码最多执行一次。

最大运行时间受程序长度限制的程序称为to run in constant time。这并不意味着每次运行时都执行相同数量的步骤。这意味着存在一个常数k，这样程序运行的步数就不会超过k步。这意味着运行时间不会随着程序输入的大小而增长。

固定时间程序的功能非常有限。例如，考虑编写一个程序来统计选举中的选票。如果一个人能编写一个程序，有限的时间内做到统计没有上限数量的选票，那将是非常令人惊讶的。事实上，可以证明这是不可能的。对问题内在难度的研究是计算复杂性的主题。在本书中，我们将多次回到这个话题。

幸运的是，我们只需要一种编程语言构造，即迭代，就可以编写任意复杂度的程序。我们在第2.4节中谈到了这一点。

### 2.3 Strings and Input

str类型的对象用于表示字符串。 str类型的文本可以使用单引号或双引号编写，例如‘abc’或“abc”。文字“123”表示一个由三个字符组成的字符串，而不是数字一百二十三。

如果试着在python中输入
<!--代码5-->
```python
'a'*'a'
```

则程序会报错

TypeError: can't multiply sequence by non-int of type 'str'

因为a不是任何类型的变量，所以解释器将其视为名称（name）。但是，由于该名称没有绑定到任何对象（object），因此尝试使用它会导致运行时错误。

字符串是Python中的几种序列类型之一。它们与所有序列类型共享以下操作。

•使用len函数可以找到字符串的长度。例如，len（'abc'）的值是3。

•索引（index）可用于从字符串中提取单个字符。在Python中，所有索引都是以0为开头的。例如，在解释器中键入“abc”[0]将导致解释器显示字符串“a”。键入“abc”[3]将产生错误消息IndexError:字符串索引超出范围。由于Python使用0表示字符串的第一个元素，因此长度为3的字符串的最后一个元素是使用索引2访问的。负数用于从字符串的末尾索引。例如，“abc”[-1]的值是“c”。

•silicing用于提取任意长度的子串，如果s是一个字符串（string）那么表达式

<!--代码6-->
```python
s[start:end]
```
即可索引到start所表示的数字到end所表示的数字-1的子字符串（substring），举例来说，'abc'[1:3]='bc'，如果省略冒号前面的值，则默认为0；如果省略冒号后面的值，则默认为字符串的长度

### 2.3.1 Input

python3有一个函数input，可以用来直接从用户那里获取输入。
它接受字符串作为参数，并在shell中显示为提示。然后等待用户键入内容，然后按enter键。用户键入的行被视为字符串，并成为函数返回的值。

Python代码中经常使用类型转换。我们使用类型的名称将值转换为该类型。例如，int（'3'）*4的值是12。当一个float被转换成int时，这个数字会被截断（不是四舍五入），例如int（3.9）的值就是int 

### 2.3.2 A Digression About Character Encoding

多年来，大多数编程语言都使用一种称为ASCII的标准来表示字符的内部表示。该标准包括128个字符，足以代表英语文本中出现的常用字符集，但不足以涵盖世界所有语言中出现的字符和重音。

近年来，人们开始转向Unicode。Unicode标准是一种字符编码系统，旨在支持所有语言书面文本的数字处理和显示。该标准包含12万多个不同的字符，涵盖129个现代和历史文字以及多个符号集。Unicode标准可以使用不同的内部字符编码来实现。你可以以以下的代码形式插入一个注释来告诉python你想要选择那种编码

```python
# -*- coding: encoding name -*-
```

可以在程序的第一行或第二行中插入，比如说

```python
# -*- coding: utf-8 -*-
```

指示Python使用UTF-8编码类型，这是万维网页面最常用的字符编码。一般而言，如果没有在程序的开头注释编码类型，python将会自动使用UTF-8类型

而当使用UTF-8时，你可以在编辑器中直接输入以下的代码

```python
print('Mluvíš anglicky?')
print('क्या आप अंग्रेज़ी बोलते हैं?')
```

shell中会输出

Mluvíš anglicky?
क्या आप अंग्रेज़ी बोलते हैं?

### 2.4 Iteration（迭代）

在结束第2.2节时，我们注意到大多数计算任务不能使用分支程序来完成。例如，考虑编写一个程序，询问用户要打印多少次字母X，然后打印一个带有该数字X的字符串。我们也许会想要编写下面的程序

```python
numXs = int(input('How many times should I print the letter X? '))
toPrint = ''
if numXs == 1:
    toPrint = 'X'
elif numXs == 2:
    toPrint = 'XX'
elif numXs == 3:
    toPrint = 'XXX'
#...
print(toPrint)
```



但很快就会发现，我们需要的条件和正整数一样多，而且正整数的数量是无限的。我们需要的是一个下面的条件

```python
numXs = int(input('How many times should I print the letter X? '))
toPrint = ''
concatenate X to toPrint numXs times
print(toPrint)
```

当我们想让一个程序多次做同样的事情时，我们可以使用迭代。
图2.4的boxedin部分显示了一种通用的迭代（也称为循环）机制。与条件语句一样，它以测试开始。如果测试的结果为True，程序将执行一次循环体，然后返回以重新评估测试。重复此过程，直到测试的计算结果为False，然后控制传递给迭代语句后面的代码。

我们可以使用while语句编写图2.4中描述的循环。考虑以下示例：

```python
# Square an integer, the hard way
x = 3
ans = 0
itersLeft = x
while (itersLeft != 0):
     ans = ans + x
     itersLeft = itersLeft - 1
print(str(x) + '*' + str(x) + ' = ' + str(ans))
```



![image-20210508141613302](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210508141613302.png)

这个代码存在一个问题，如何解决x<0时的情况？当x<0时，每一次循环都会将x变得愈来愈小并且一直远离0，这会使程序一直运行下去。一种解决方案是将itself变量在初始化时初始化为x的绝对值，不过这会使输出结果为负值，不过我们只要对ans稍加改动即可，比如ans=ans+abs（x)，问题就解决了

使用‘break’可以在不用测试循环条件的情况下退出循环，并紧接着执行位于整体循环后面的代码，比如

```python
#Find a positive integer that is divisible by both 11 and 12
x = 1
while True:
   if x%11 == 0 and x%12 == 0:
        break
   x = x + 1
print(x, 'is divisible by 11 and 12')
```

的输出是

132 is divisible by 11 and 12

如果在嵌套循环（另一个循环中的循环）内执行break语句，则break将终止内部循环。
现在我们已经介绍了Python的几乎所有知识，这些知识是我们开始编写处理数字和字符串的有趣程序所需要的。

### 3 SOME SIMPLE NUMERICAL PROGRAMS

既然我们已经介绍了一些基本的Python构造，现在是时候开始考虑如何组合这些构造来编写一些简单的程序了。
在这个过程中，我们将偷偷地介绍一些更多的语言结构和一些算法技术。

### 3.1 Exhaustive Enumeration（穷举）

下面的代码表示求一个输入整数的立方根，如果输入数字的立方根非整数，会输出一行消息

```python
#Find the cube root of a perfect cube
x = int(input('Enter an integer: '))
ans = 0
while ans**3 < abs(x):
    ans = ans + 1
if ans**3 != abs(x):
    print(x, 'is not a perfect cube')
else:
    if x < 0:
       ans = -ans
    print('Cube root of', x,'is', ans)
```

这个程序会在x取何值时终止？答案是“所有整数”，这一点很简单。

•表达式ans**3的值从0开始，每次通过循环都会变大。

•当达到或超过abs（x）时，循环终止。

•由于abs（x）始终为正，因此在循环终止之前，迭代次数必然有限。

当你在编写一个循环时，都应该考虑适当的递减函数（decrementing function）。这是一个具有以下属性的函数

• It maps a set of program variables into an integer.

• When the loop is entered, its value is nonnegative.

• When its value is ≤ 0, the loop terminates.

• Its value is decreased every time through the loop.

当我们将程序中的'ans=ans+1'修改为'ans=ans'时

程序将永远运行，因为循环体不再缩短ans**3和abs（x）之间的距离。当遇到一个似乎不会终止循环的程序时，有经验的程序员经常插入print语句，比如这里的语句，以测试递减函数是否确实在递减。
在这个程序中使用的算法技术是一个称为穷举法或枚举法的方法。我们列举所有的可能性，直到我们得到正确的答案或用尽可能的空间。乍一看，这似乎是一种极其愚蠢的解决问题的方法。然而，令人惊讶的是，穷举枚举算法通常是解决问题的最实用的方法。它们通常易于实现和理解。而且，在许多情况下，它们的运行速度足以满足实际用途。确保删除或注释掉插入的print语句并重新插入语句ans=ans+1，然后尝试查找1957816251的立方根。程序几乎会在瞬间完成。现在，试7406961012236344616

如你所见，即使需要数百万次的猜测，这通常也不是问题。现代计算机速度惊人。执行一条指令仅需要一纳秒到十亿分之一秒的时间。

### 3.2 For Loops

我们现在为止所使用的while语句是高度固定化的，为了简化这类迭代程序，python提供了一种for语言机制，其一般形式是

for variable in sequence:

code block

for后面的变量绑定到序列中的第一个值，并执行代码块。然后，该变量被赋予序列中的第二个值，并且再次执行代码块。该过程将持续直到序列结束或在代码块内执行break语句为止

绑定到变量的值序列通常使用内置函数range生成，该函数返回一系列整数。range函数按顺序接受三个整数参数：start、stop和step。它会产生这样的指令：start，start+step，start+2*step，等等。假如step是正数，那么这个序列的最后一个元素是小于stop所代表的整数的最大的start+i*step

换言之，这是一个等差数列，start表示等差数列的第一项；step表示步长（公差）；而stop则表示这个数列所能允许的最大值（数列中的元素不能超过这个值，等于也不行）

在step小于0时，同理我们可以得到以上的规则，不同的是，这时stop表示的是这个数列所能允许的最小值

举例来说，range(5, 40, 10)可以得到一个元素为5，15，25，35的序列；而range(40, 5, -10)则会得到一个元素为40，30，20，10的序列。如果省略第一个参数（起点），则系统会默认它时0，而如果省略最后一个参数（步长），那么系统会默认它是1

考虑以下的代码

```python
x = 4
for i in range(0, x):
     print(i)
```

其输出是0123

但如果我们将代码修改如下

```python
x = 4
for i in range(0, x):
      print(i)
      x = 5
```

这里有一个问题，即在循环中更改x的值是否会影响迭代次数。事实上并没有，for行中range函数的参数在循环的第一次迭代之前即进行求值，而不是在随后的迭代中重新求值（注：在进行了一次迭代以后，x的值已经被修改成5，但这并不影响序列的范围），在脱离这个循环以前，序列的范围都不会被改变，但在循环嵌套中这一点有所改变，例如

```python
x = 4
for j in range(x):
   for i in range(x):
       print(i)
       x = 2
```

的输出是

0
1
2
3
0
1
0
1
0
1

原因在于当j=0时，进入第一次循环，此时x=4，因此序列的范围还未改变；而当第一次循环结束时，x的值已经被修改成2，因而在进入i的第二次循环时（此时外部循环还未结束，j取到序列的第二个值1），对于第二个循环来讲，x=4这件事已经是过去的事了，现在x=2，故只会输出01.

换言之，外循环中的range函数只求值一次，而内循环中的range函数则在每次开始for语句时求值。

图3.2中的代码重新实现了寻找立方根的穷举枚举算法。for循环中的break语句使循环在对其迭代的序列中的每个元素运行之前终止。

```python
#Find the cube root of a perfect cube
x = int(input('Enter an integer: '))
for ans in range(0, abs(x)+1):
    if ans**3 >= abs(x):
        break
if ans**3 != abs(x):
    print(x, 'is not a perfect cube')
else:
    if x < 0:
         ans = -ans
    print('Cube root of', x,'is', ans)
```

for语句可以与in运算符结合使用，以方便地对字符串的字符进行迭代。例如，

```python
total = 0
for c in '12345678':
    total = total + int(c)
print(total)
```

### 3.3 Approximate Solutions and Bisection Search（近似解和对分搜索）

想象一下有人要求你编写一个找到任何非负数的平方根的程序。 你该怎么办？

你也许会想要一个更精确的问题描述。例如，如果要求找到2的平方根，程序应该怎么做？  2的平方根不是有理数。 这意味着无法将其值精确地表示为有限的数字字符串（或浮点数），因此无法解决最初提出的问题。

正确的要求是写一个找到一个平方根近似值的程序，即，一个与实际平方根足够接近的答案才有用。 我们将在本书的后面部分非常详细地讨论这个问题。 但是现在，让我们考虑“足够接近”作为实际答案的某个常数（称为ε）之内的答案。

下面的代码描述了一个估算平方根的程序，在这里他用了一个我们此前从未用过的符号“+=”用于代替“ans=ans+1”这一程序，对于*=，-=而言也是如此

```python
x = 25
epsilon = 0.01#精度
step = epsilon**2#步长
numGuesses = 0
ans = 0.0
while abs(ans**2 - x) >= epsilon and ans <= x:
   ans += step
   numGuesses += 1
print('numGuesses =', numGuesses)
if abs(ans**2 - x) >= epsilon:
   print('Failed on square root of', x)
else:
   print(ans, 'is close to square root of', x)
```

这是采用穷举算法来求解平方根的一个例子

我们应该对程序没有发现25是一个完美的平方数而失望吗？事实上并非如此，因为程序已经达到了预期效果，输出5和输出一个很接近5的数字并无二致

如果我们将x设置为0.25，您认为会发生什么？ 会找到接近0.5的根吗？ 不。 它将报告

```python
numGuesses = 2501
Failed on square root of 0.25
```

报错的原因很简单，对于大于1的数而言，其平方根必然比其自身要小，因此其平方根始终满足while语句中的ans<=x的条件，但对于小于1的输入则不然。解决方法也很直白，将其改为ans**<=x即可

现在，让我们考虑一下该程序将运行多长时间。 迭代次数取决于答案与0的接近程度以及步长的大小。

粗略地说，该程序将最多执行x / step时间的while循环。让我们尝试使用更大的数字，例如x =123456。它将运行一段时间，然后打印 

```python
numGuesses = 3513631
Failed on square root of 123456
```

为什么会这样？毫无疑问，一定存在一个精度为0.01的数是123456的平方根，但我们的程序却找不到它。原因在于我们的步长太大，使程序跳过了正确答案，但若我们将步长再更改的更小一些，比如step=epsilon**3，程序运行的时间会变得更长，

如果步长改为0.000001，那么要多少次循环才能找到123456的平方根？，123456的平方根大约是351.6，这意味着计算机要做351000000次循环才能找到答案

因此我们需要一个不同的算法来解决这个问题，我们需要一个更好的算法。不过在我们开始工作以前，我们先来看看一个问题，这个问题乍一看与这个问题毫无关联。

考虑一个在英语词典中搜索给定字母序列的单词的问题，原则上，这个问题可以采用穷举法，你可以从第一个单词开始搜索，然后检查每个单词，直到找到以某些给定字母序列开头的单词；或者不幸的，字典中也许不包含这个单词，假设字典中有n'个单词，那么这次不幸的的搜索需要进行n次。不过就常识而言，在字典的出版过程中，人们会把相同字母开头的单词聚集在一起并为他们标号，大大减少了搜索时间。这样，当人们在查找单词时，不会漫无目的的从第一个单词开始查起，而是有目的的定位到某一个索引中

现在让我们把这个思想带入到这个问题中，假设在搜索前，我们已事先知道了x的平方根的良好近似值介于0和max之间。我们可以利用数字有序这一事实（即对于两个数字n1和n2而言，只可能存在n1<n2或n1>n2这两种结果）来简化算法

在[0,max]这个区间内，我们由于不知道具体数值，因此我们可以随意选择搜索起点，比如从中间开始，这样就分成了两个区间[0,guess]和[guess,max]

假如guess并非正解（大部分时间都不是）那么我们下一步判断这个值是过大还是过小，比如说是过大，那么下一步的检索位置就要在guess的左侧开始，并重复上述过程

```Python
x = 25
epsilon = 0.01
numGuesses = 0
low = 0.0
high = max(1.0, x)
ans = (high + low)/2.0
while abs(ans**2 - x) >= epsilon:
      print('low =', low, 'high =', high, 'ans =', ans)#debug
      numGuesses += 1
      if ans**2 < x:
          low = ans
      else:
           high = ans
      ans = (high + low)/2.0
print('numGuesses =', numGuesses)
print(ans, 'is close to square root of', x)
```

请注意，它找到的答案与我们之前的算法不同。 不过这无伤大雅

 更重要的是，请注意，在循环的每次迭代中，要搜索区间的大小都会减少一半。 由于它在每一步将搜索区间分成两半，因此称为对分搜索。 对分搜索是对我们先前算法的巨大改进，此前的算法在每次迭代时仅减少了很小的搜索空间。

让我们再次尝试x = 123456。 这次，程序只需要三十个猜测就可以找到可接受的答案。  x = 123456789怎么样？ 仅需四十五个猜测。

这个算法事实上并无特殊之处，如果我们将while条件中的2改为3那么我们就能求得立方根，在第四章中我们会介绍一种语言机制以找到任意数的任意次方根

### 3.4 A Few Words About Using Floats

在大多数情况下，float类型的数字提供了与实数相当好的近似值。 但是“大多数情况下”并非总是如此，如果不这样做，可能会导致意想不到的后果。 例如，尝试运行代码

```python
x = 0.0
for i in range(10):
     x = x + 0.1
if x == 1.0:
     print(x, '= 1.0')
else:
     print(x, 'is not 1.0')s
```

理论上，这个程序会运行10次，最终使x=1.0，但事实上，最后的输出结果是

0.9999999999999999 is not 1.0

出现这个结果的原因在于计算机与人们平时所采用的进制不同，计算机采用二进制，人们平时可以用0123456789来表示所有数字（十进制）。长度为一的序列可以表示十个数字，而长度为二的序列可以表示100个数字。二进制的原理与其类似，长度为n的数列可以表示2的n次方个数字

也许因为大多数人有十根手指，我们似乎喜欢使用小数表示数字。 另一方面，所有现代计算机系统都以二进制表示数字。 这不是因为计算机天生就有两个手指。 这是因为很容易构建硬件开关，即仅处于打开或关闭两种状态之一的设备。 计算机使用二进制表示形式，而人们使用十进制表示形式可能会导致偶尔的认知失调。

在几乎所有的现代编程语言中，非整数是使用称为浮点的表示形式实现的。让我们假设内部表示形式为十进制。 浮点表示法允许我们将数字表示为一对整数构成的数对，其中左边是系数，右边是指数。 例如，数字1.949将表示为对（1949，-3），代表乘积1949 * 10-3（1949乘以十（十进制）的负三次）。

有效数字的位数确定可以表示数字的精度。 例如，如果只有两个有效数字，则不能准确表示数字1.949。 必须将其转换为1.949的近似值，在这种情况下为1.9。 该近似值称为四舍五入值。

现代计算机使用二进制（而不是十进制）表示形式。 我们用二进制而不是十进制表示有效数字和指数，并将底数变为2而不是10。 例如，数字0.625（5/8）将被表示为对（101，-11）； 因为5/8是二进制形式的0.101，而-11是-3的二进制形式，所以对（101，-11）表示5 * 2-3 = 5/8 = 0.625。

那么在python里0.1应该如何采用二进制形式表示？最好的拟合是（0011，-101），这个数实际上是3/32，而假如我们拥有五位有效数字（二进制数位），0.1就会是（11001，-1000），相当于25/256，我们需要多少位数才能用二进制表示0.1呢？答案是无穷位，因为不存在整数sig和exp使sig*2的-exp次方=0.1.因此python（或者其他语言）都只能用近似值来表示0.1

此外我们介绍一个round函数，表达式round（x，numDigits）返回的浮点数将会是将x的值四舍五入到小数点后的numDigits个数的十进制数字。 例如，print round（2 ** 0.5，3）将打印1.414作为2的平方根的近似值。

实数和浮点数之间的差异真的重要吗？幸运的是，大多数时候情况并非如此。 只有在少数情况下，我们只能接受是1.0，而不能接受0.9999999999999999。 但是，几乎总是值得担心的一件事就是相等性的测试。 如我们所见，使用==比较两个浮点值可能会产生令人惊讶的结果。 一般而言，我们的测试标准是两个浮点数是否足够接近，而非是否完全相等。 因此，举例而言，在判断两个浮点数是否相等时最好写abs（x-y）<0.0001而不是x == y。

另一件事需要担心的是舍入误差的累积。 多数情况下，一切正常，因为有时存储在计算机中的数字比预期的要大一些，有时甚至比预期的要小一些。 但是，在某些程序中，错误全都朝同一个方向累积，并随着时间的推移而累积。

### 3.5 Newton-Raphson

牛顿法求近似值是最为常用的近似算法，这个方法可以用来求出许多多项式函数的实根，不过在本书中，我们只关心只有一个变量的多项式的实根。事实上，它可以很方便的扩展到多变量方程中

单变量多项式由0或一系列包含变量，系数和指数的非零项构成，其次数由多项式内最大的指数决定，一般而言变量在分数线下或根号内的不算做多项式。

假如p是一个多项式而r是一个实数，我们记p（r）为x=r时的多项式的值，而多项式的根指的是p=0时x的值

牛顿证明了一个定理，假设存在一个值，记为guess，是一个多项式的近似根，那么
$$
guess-p(guess)/p^`(guess)
$$
会是一个近似度更好的解，这个方法称为逐次逼近（successive approximation）

下面展示了一个如何求得平方根的代码

```python
#Newton-Raphson for square root
#Find x such that x**2 - 24 is within epsilon of 0
epsilon = 0.01
k = 24.0
guess = k/2.0
while abs(guess*guess - k) >= epsilon:
    guess = guess - (((guess**2) - k)/(2*guess))
print('Square root of', k, 'is about', guess)
```

# 4 FUNCTIONS, SCOPING, AND ABSTRACTION

到目前为止，我们已经介绍了数字，赋值，输入/输出，比较和循环构造。  Python的这个子集有多强大？ 从理论上讲，我们可利用上述构造来实现任意可实现的功能，即它是图灵完整的。 这意味着，如果可以通过计算解决问题，那么上面所学的知识已经足以解决这个问题

不过，这并非是说我们只能使用这些命令。 至此，我们已经介绍了许多语言机制，但是代码只是一个单一的指令序列，所有指令都合并在一起。 例如，在上一章中，我们查看了图4.1中的代码。

```python
x = 25
epsilon = 0.01
numGuesses = 0
low = 0.0
high = max(1.0, x)
ans = (high + low)/2.0
while abs(ans**2 - x) >= epsilon:
      print('low =', low, 'high =', high, 'ans =', ans)#debug
      numGuesses += 1
      if ans**2 < x:
          low = ans
      else:
           high = ans
      ans =(high + low)/2.0
print('numGuesses =', numGuesses)
print(ans, 'is close to square root of', x)
```

这是一段合理的代码，但是缺乏通用性。 它仅适用于变量x和epsilon表示的值。 这意味着如果要在其他地方重新用到它，我们需要复制代码，可能还伴随着重新编辑变量名的问题，然后才可以将其粘贴到需要的地方。 因此，我们无法在其他更复杂的计算中轻松使用此计算

进一步的，如果我们要计算立方根而非平方根，我们还要重新编辑代码来满足我们的要求，如果我们要同时计算立方根和平方根呢？这个程序会包含许多几乎相同的代码块。这是非常不好的事情。 程序包含的代码越多，出现问题的机会就越大，并且代码维护的难度就越大。 例如，想象一下，平方根的初始实现中存在错误，并且在测试程序时发现了该错误。 在一个地方修复平方根的实现很容易，但却有可能因此而忘了在其他地方也有类似的代码也需要修复。

Python提供了几种语言功能，使代码的泛化和重用相对容易。 最重要的是函数

### 4.1 Functions and Scoping

事实上我们已经使用了许多python内置的函数，但是我们也可以自己定义函数

### 4.1.1 Function Definitions

在python中，任何函数定义都具有以下的形式

```python
def name of function (list of formal parameters):
    body of function
```

例如

```python
def maxVal(x, y):
    if x > y:
       return x
    else:
       return y
```

def是一个保留字，它告诉Python函数即将被定义。 函数名称（在此示例中为maxVal）只是一个用于引用该函数的名称

在函数名称后括号内的两个参数被称为函数的形式参数（简称形参），在函数被调用时，形参将会和进入函数的实际参数（简称实参）绑定

函数体可以是任何一段Python代码。但是，有一个特殊的语句return，它只能在函数体中使用。

函数调用是一个表达式，与所有表达式一样，它也有一个值。该值是被调用函数返回的值。例如，表达式maxVal（3,4）*maxVal（3,2）的值是12，因为第一次调用maxVal返回int 4，第二次调用返回int 3。注意，return语句的执行终止了对函数的调用。

当函数被调用时

1.计算构成实际参数的表达式，并将函数的形式参数绑定到结果值。例如，调用maxVal（3+4，z）将形式参数x绑定到7，形式参数y绑定到变量z将会在计算时调用时z拥有的值。

2.执行点（要执行的下一条指令）从调用点移动到函数体中的第一条语句。

3.函数体中的代码将一直执行，直到遇到return语句（在这种情况下，return后面的表达式的值将成为函数调用的值），或者不再有要执行的语句（在这种情况下，函数将不返回值）(如果return后没有表达式，则调用的值为None。）

4.被调用函数的值就是函数返回的值。

5.执行点在调用之后立即转移回执行源代码。

函数的参数提供了一种名为“lambda abstraction”的东西，我们马上就会看到，我们现在所说的函数比数学上所定义的函数的范围要大得多，“lambda abstraction”允许程序员编写的代码并非是指定特定的对象，而可以是通过函数调用这一命令来选择用作实参的任意对象

### 4.1.2 Keyword Arguments and Default Values（关键字参数和默认值）

在Python中，有两种方法可以将形式参数绑定到实际参数。
最常用的方法是positional（也就是按位置顺序从左到右给形参赋值），这是我们迄今为止唯一使用的方法。第一个形式参数绑定到第一个实际参数，第二个形式参数绑定到第二个实际参数，等等。Python还支持关键字参数，其中形式参数使用形式参数的名称绑定到实际值。考虑函数定义 

```python
def printName(firstName, lastName, reverse):
    if reverse:
         print(lastName + ', ' + firstName)
    else:
         print(firstName, lastName)
```

函数printName假设firstName和lastName是字符串，reverse是布尔值。如果reverse==True，则打印lastName、firstName，否则打印firstName lastName。
以下每一项都是对printName的等效调用：

```python
printName('Olga', 'Puchmajerova', False)
printName('Olga', 'Puchmajerova', reverse = False)
printName('Olga', lastName = 'Puchmajerova', reverse = False)
printName(lastName = 'Puchmajerova', firstName = ' Olga',reverse = False)
```

尽管关键字参数可以以任何顺序出现在实际参数列表中，但在关键字参数后面加上非关键字参数是不合法的。
例如

```python
printName('Olga', lastName = 'Puchmajerova', False)
```

在上面的错误范例中，关键字参数‘lastname’后面加上了一个‘false’，尽管函数调用的参数中确实有一个布尔值变量，但由于是在关键字参数后面，因此必须也写成关键字参数的形式

关键字参数通常与默认参数值（defalut parameter values)一起使用。例如，

```python
def printName(firstName, lastName, reverse = False):
    if reverse:
         print(lastName + ', ' + firstName)
    else:
         print(firstName, lastName)
```

默认值允许程序员使用少于指定数量的参数调用函数。在这里，函数在定义时已经事先声明了布尔值为false，在调用函数时，如果不说明布尔值为何，则默认为false，例如

```python
printName('Olga', 'Puchmajerova')
printName('Olga', 'Puchmajerova', True)
printName('Olga', 'Puchmajerova', reverse = True)
```

的输出是

```python
Olga Puchmajerova
Puchmajerova, Olga
Puchmajerova, Olga
```

printName的最后两个调用在语义上是等价的。最后一种方法的优点是为可能存在的true提供了回旋余地

###  4.1.3 Scoping（范围界定）

让我们看看下面这个例子

```python
def f(x): #name x used as formal parameter
   y = 1
   x = x + y
   print('x =', x)
   return x

x = 3
y = 2
z = f(x) #value of x used as actual parameter
print('z =', z)
print('x =', x)
print('y =', y)
```

当其运行时，其输出是

```python
x = 4
z = 4
x = 3
y = 2
```

这是怎么回事？在调用f时，形式参数x将会被赋予实际参数x的值。需要注意的是，尽管实际参数和形式参数具有相同的名称，但它们不是相同的变量。

每个函数定义一个新的name space，也称为作用域（scope）。f中使用的形式参数x和局部变量y只存在于f的定义范围内。函数体中的赋值语句x=x+y将变量x的值赋为4。f中的赋值行为对f范围之外的变量x和y的赋值没有任何影响。

这里有一个方法来思考这一现象

1.在顶层，即shell层次，符号表（symbol tabel）会跟踪在该层次定义的所有变量名称及这些变量名称当前被赋给的值。

2.调用函数时，会创建一个新的符号表（通常称为堆栈帧（stack frame）。此表跟踪函数中定义的所有变量名称（包括形式参数）及其当前值。如果从函数体中调用函数，则会创建另一个堆栈帧。

3.函数完成后，其堆栈帧将消失。

在Python中，可以通过查看程序文本来确定名称的范围。这称为static或lexical scoping。如下面的示例所示

```python
def f(x):
   def g():
      x = 'abc'
      print('x =', x)
   def h():
      z = x
      print('z =', z)
   x = x + 1
   print('x =', x)
   h()
   g()
   print('x =', x)
   return g


x = 3
z = f(x)
print('x =', x)
print('z =', z)
z()
```

与代码相关联的堆栈帧的历史记录如下图所示
第一列除函数f内部变量名的已知的一组变量名称，即变量x和z以及函数名f。第一个赋值语句将x绑定到3。

![image-20210513143025255](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210513143025255.png)

赋值语句z=f（x）首先通过使用x所绑定的值调用函数f来计算表达式f（x）。当输入f时，将创建一个堆栈帧，如第2列所示。堆栈框架中的名称是x（形式参数，而不是函数外的变量名x）、g和h。变量g和h与function类型的对象绑定。

这些函数的性质由f中的函数定义给出。当从f中调用h时，会创建另一个堆栈帧，如第3列所示。可以看到，该堆栈帧中仅包含局部变量z。为什么它不包含x？仅当该变量作为函数的形参或者该变量在函数体内被赋值的时候（形象地说，这个变量出现在了赋值语句的左边），才会将该名称添加到与函数关联的作用域中。在h的主体中，x只出现在赋值语句的右侧。

如果一个变量名称（在本例中为x）在函数体中（本例中是函数h）没有被赋予任何类型的值（可以是int，float等类型），则解释器会在包含这个函数名的堆栈帧中寻找这个变量名称（在本例中是定义f时所产生的堆栈帧，这个堆栈帧中包含h这一函数名）。如果找到了该变量名称（在本例中是这样），则使用它绑定到的值（4）。如果在那里找不到，则会生成错误消息。

当h返回时，与h调用相关联的堆栈帧消失（从堆栈顶部弹出），如第4列所示。请注意，我们从不从堆栈的中间删除帧，而只删除最近添加的帧。正是因为它有这种“后进先出”的行为，我们才把它称为stake（想象一下在自助餐厅里有一堆托盘等着拿）。

接下来调用g，并添加一个包含g的局部变量x的堆栈帧（第5列）。当g返回时，该帧弹出（第6列）。当f返回时，将弹出包含与f关联的名称的堆栈帧，使我们返回到原始堆栈帧（第7列）。

注意，当f返回时，即使变量g不再存在，该名称曾经绑定到的function类型的对象仍然存在。这是因为函数是对象，可以像任何其他类型的对象一样返回。

因此，z可以被赋予f返回的值，函数call z（）可以用来调用在f中绑定到名称g的函数，即使函数g在函数f之外根本没有被定义

从而该代码的输出是

```python
x = 4
z = 4
x = abc
x = 4
x = 3
z = <function f.<locals>.g at 0x1092a7510>
x = abc
```

在函数体中，假如要使用本地变量，这个本地变量的赋值语句必须写在所有的表达式和命令之前，这是因为假如在一个函数体中出现了对一个变量的赋值语句，则即使该赋值语句是出现在一个表达式或者一条命令的后面，它也将会被视作该函数中的局部变量，这回出现一些问题，例如

```python
def f():
    print(x)
def g():
    print(x)
    x = 1
x = 3
f()
x = 3
g()
```

在执行代码后，程序会报错

```python
UnboundLocalError: local variable 'x' referenced before assignment
```

这是因为print语句后面的赋值语句导致x变为g的局部变量。因为x是g的局部变量，所以在执行print语句时它没有值（还未被赋值）。 

### 4.2 Specifications

下面的代码定义了一个函数findRoot，它包含了我们在此前所提出的对分搜索算法。它还包含一个函数testFindRoot，可以用来测试findRoot是否按预期工作

```python
def findRoot(x, power, epsilon):
     """Assumes x and epsilon int or float, power an int,
                 epsilon > 0 & power >= 1
        Returns float y such that y**power is within epsilon of x.
               If such a float does not exist, it returns None"""
     if x < 0 and power%2 == 0: #Negative number has no even-powered
                        #roots
        return None
    low = min(-1.0, x)
    high = max(1.0, x)
    ans = (high + low)/2.0
    while abs(ans**power - x) >= epsilon:
         if ans**power < x:
                low = ans
         else:
                high = ans
         ans = (high + low)/2.0
    return ans

def testFindRoot():
    epsilon = 0.0001
    for x in [0.25, -0.25, 2, -2, 8, -8]:
        for power in range(1, 4):
             print('Testing x =', str(x), 'and power = ', power)
             result = findRoot(x, power, epsilon)
             if result == None:
                  print('  No root')
             else:
                  print(' ', result**power, '~=', x)
```

函数testFindRoot几乎和findRoot本身一样长。对于没有经验的程序员来说，编写这样的测试函数似乎常常是一种浪费。然而，经验丰富的程序员知道，在编写测试代码方面的投资往往会带来巨大的回报。它当然比在调试过程中一次又一次地在shell中输入测试用例要好得多（找出程序不工作的原因，然后修复它的过程）。这也迫使我们思考哪些测试可能最具启发性。
三个引号之间的文本在Python中称为docstring。按照惯例，Python程序员使用docstring来提供函数的规范。可以使用内置函数help访问这些docstring。例如，如果我们进入shell并键入help（abs），系统将显示

```python
Help on built-in function abs in module built-ins:
    
abs(x)
     Return the absolute value of the argument.
```

而如果我们在shell中输入help（findRoot），shell就会显示

```python
findRoot(x, power, epsilon)
Assumes x and epsilon int or float, power an int,
epsilon > 0 & power >= 1
Returns float y such that y**power is within epsilon of x.
If such a float does not exist, it returns None
```

如果我们在编辑器中输入findRoot（，则将显示形式参数列表。

函数的specification定义了函数的实现者和那些编写函数的程序员之间的约定。我们称函数的使用者为client。这个约定包含两部分：

•Assumptions：所谓的“假设”描述了使用者在使用函数时必须满足的条件。通常，它们描述对实际参数的约束。“假设”会为每个参数（或者其中的数个）指定可接受的类型集（比如进入函数的参数应该满足一些什么条件，否则会报错或者返回none），并且经常对一个或多个参数的值进行一些约束。
例如，findRoot的docstring的前两行描述了findRoot的使用者（调用时）必须满足的假设。
•Guarantee：这些描述了函数必须满足的条件（即函数的功能，函数必须返回什么样的值），（前提是函数以满足假设的方式调用）。findRoot的docstring的最后两行描述了函数实现必须满足的保证。

函数是一种产生计算元素的方式，就像我们的内置函数max或者abs一样，我们希望产生一个内置函数进行求根操作或者其他的复杂操作，函数通过将我们的目的分解开和将这个目的抽象化做到了这一点

分解（decomposition）产生了结构。它允许我们将程序分解为许多互相之间独立的部分，就像线性空间中的基向量，这些部分之间互相组合，又能构成一个完整的程序

抽象（abstraction）隐藏细节。它允许我们使用像一个黑匣子一样的代码，也就是说，它的内部细节我们看不到，实际上，我们不需要看到，甚至不应该看到。抽象的本质是保存在给定上下文中相关的信息，而忽略在该上下文中无关的信息。在编程中，我们需要真正了解我们编程的目的是什么，明白我们想要什么，并通过简明扼要的手法实现这一点，这才是真正的编程艺术。

### 4.3 Recursion（递归）

你也许听说过递归，并且很可能认为它是一种相当高深的编程技术。其实这只是外界的误解。递归是一个非常重要的概念，但它并不那么高深，它也不仅仅是一种编程技术。

作为一种描述性方法，递归被广泛使用，即使是那些从未想过要编写程序的人，他们在日常生活中也会经常碰到“递归”这一概念。想想美国法典中定义“天生”公民概念的一部分。大致来说，定义如下

•任何在美国境内出生的孩子，

•任何在美国境外结婚出生的孩子，只要父母一方在孩子出生前在美国居住，以及

•任何在美国境外婚生子女，其父母之一是美国公民，且在子女出生前至少在美国居住了五年，前提是这些年中至少有两年是在该公民的十四岁生日之后

第一点十分简单易懂，如果你出生在美国，你就是一个天生的美国公民（比如巴拉克奥巴马）。如果你不是在美国出生的，那么决定你是否是美国公民的因素在于你的父母是不是美国公民（自然出生或归化）。而要确定你的父母是否是美国公民，你可能得看看你的祖父母，等等。

一般来说，递归定义由两部分组成。至少有一个base case会直接指定特殊情况的结果（上例中的情况1），并且至少有一个递归（归纳）情况（上例中的情况2和3）根据某个其他问题的答案来定义答案，通常是同一问题的更简单版本。

世界上最简单的递归定义可能是自然数的阶乘这一概念（通常在数学中使用！表述）。经典的归纳定义是
$$
1！=1
$$

$$
(n+1)!=(n+1)*n!
$$

第一个等式定义了基本情况。第二个等式定义了除基本情况外的所有自然数的阶乘，即前一个数的阶乘。

下面的代码包含了阶乘的迭代（factI）和递归（factR）实现。

```python
def factI(n):                   def factrR(n):
"""Assumes n an int > 0         """Assumes n an int > 0 Returns n!"""                   Returns n!"""
result = 1                      if n == 1:
while n > 1:                       return n
   result = result * n          else:
   n-=1                            return n*factR(n - 1)
return result

```

这个函数非常简单，用两种方法都不难实现。不过，第二个是对原始递归定义的更贴切的解释。

从factR的内部调用factR来实现factR几乎像是作弊。它的工作原理与迭代实现的工作原理相同。我们知道迭代实际上会终止，因为n开始时是正的，每次循环都会减少1。这意味着它不能永远大于1。类似地，如果用1调用factR，它将返回一个值而不进行递归调用。当它确实进行递归调用时，它总是使用比调用它时使用的值小一的值来执行。最终，递归终止于调用factR（1）。

### 4.3.1 Fibonacci Numbers（斐波那契数列）

斐波那契数列是另一种常用的数学函数，通常以递归方式定义。  “它们像兔子一样繁殖”，通常用于描述说话者认为增长过快的种群。  1202 年，意大利数学家比萨的莱昂纳多，也被称为斐波那契，开发了一个公式来量化这个概念，尽管有一些不太现实的假设。假设一对刚出生的兔子，一雄一雌，被放入 在笔中（或更糟糕的是，在野外释放）。 进一步假设兔子能够在一个月大的时候交配（令人惊讶的是，有些品种可以）并且有一个月的妊娠期（令人惊讶的是，有些品种可以）。 最后，假设这些神话中的兔子永远不会死，并且雌性从第二个月开始每个月都会产生一对新的兔子（一只雄性，一只雌性）。六个月后会有多少只母兔？

在第一个月的最后一天（称为第 0 个月），将有一个女性（准备在下个月的第一天受孕）。 在第二个月的最后一天，仍然只有一个女性（因为她要到下个月的第一天才会分娩）。 下个月的最后一天，会有两只雌性（一只怀孕，一只没有）。 在下个月的最后一天，将出现三只女性（两只怀孕，一只未怀孕）。 等等。 让我们以表格的形式看看这个进展，图 4.6。

请注意，对于第 n > 1 个月，女性 (n) = 女性 (n-1) + 女性 (n-2)。 这不是意外。 每个在第 n-1 个月还活着的女性在第 n 个月仍然活着。 此外，每个在第 n-2 个月存活的雌性都会在第 n 个月产生一个新的雌性。 可以将新的雌性添加到第 n-1 个月存活的雌性中以获得第 n 个月的雌性数量。

![image-20210831100842350](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210831100842350.png)

人口的增长自然地用复发来描述

```python
females(0) = 1
females(1) = 1
females(n + 2) = females(n+1) + females(n)
```

此定义与阶乘的递归定义略有不同： 

• 它有两个基本情况，而不仅仅是一个。 通常，您可以根据需要拥有任意数量的基本案例。

• 在递归情况下，有两个递归调用，而不仅仅是一个。 同样，您可以根据需要设置多个。

图 4.7 包含 Fibonacci 递归的直接实现，以及可用于测试它的函数。

```python
def fib(n):
     """Assumes n int >= 0
        Returns Fibonacci of n"""
      if n == 0 or n == 1:
          return 1
      else:
          return fib(n-1) + fib(n-2)
def testFib(n):
    for i in range(n+1):
        print('fib of', i, '=', fib(i))
```

虽然显然是正确的，但这是斐波那契函数的一个非常低效的实现。有一个简单的迭代实现要好得多。

编写代码是解决这个问题的简单部分。 一旦我们从一个关于兔子的问题的模糊陈述变成了一组递归方程，代码几乎是自己写的。 寻找某种抽象方法来表达手头问题的解决方案，通常是构建有用程序最困难的一步。 我们将在本书后面详细讨论这一点。

正如您可能猜到的那样，这对于野外兔子种群的增长来说并不是一个完美的模型。  1859 年，澳大利亚农民托马斯·奥斯汀从英国进口了 24 只兔子，用作狩猎的目标。 十年后，澳大利亚每年约有 200 万只兔子被射杀或困住，对人口没有明显影响。 这是很多兔子，但离第 120 斐波那契数不远。

虽然斐波那契数列实际上并没有提供兔子种群增长的完美模型，但它确实具有许多有趣的数学特性。 斐波那契数列在自然界中也很常见。

### 4.3.2 Palindromes（回文）

递归对于许多不涉及数字的问题也很有用。 图 4.8 包含一个函数 isPalindrome，它检查字符串的前后读取方式是否相同。

函数 isPalindrome 包含两个内部辅助函数。 该函数的客户应该不感兴趣，他们应该只关心 isPalindrome 是否符合其规范。 但是你应该关心，因为通过检查实现可以学到一些东西。

辅助函数 toChars 将所有字母转换为小写并删除所有非字母。 它首先使用字符串的内置方法生成与 s 相同的字符串，只是所有大写字母都已转换为小写字母。当我们进入类时，我们将更多地讨论方法调用。现在，将其视为函数调用的特殊语法。 我们没有将第一个（在这种情况下仅是）参数放在函数名称后面的括号内，而是使用点表示法将该参数放在函数名称之前。

```python
def isPalindrome(s):
   """Assumes s is a str
      Returns True if letters in s form a palindrome; False
        otherwise. Non-letters and capitalization are ignored."""
   def toChars(s):
      s = s.lower()
      letters = ''
      for c in s:
         if c in 'abcdefghijklmnopqrstuvwxyz':
            letters = letters + c
      return letters
   def isPal(s):
      if len(s) <= 1:
         return True
      else:
         return s[0] == s[-1] and isPal(s[1:-1])
   return isPal(toChars(s))
```

辅助函数 isPal 使用递归来完成真正的工作。 两个基本情况是长度为零或一的字符串。 这意味着实现的递归部分仅在长度为 2 或更多的字符串上达到。  else 子句中的连词从左到右求值。 代码首先检查第一个和最后一个字符是否相同，如果相同，则继续检查减去这两个字符的字符串是否为回文。 在此示例中，除非第一个连接词评估为 True，否则不会评估第二个连接词在语义上无关。 然而，在本书的后面，我们将看到这样的布尔表达式短路评估在语义上相关的例子。

isPalindrome 的这种实现是一个重要的问题解决原则的例子，称为分而治之。  （这个原则与分治算法有关，但略有不同，分治算法在第 10 章中讨论。）解决问题的原则是通过将一个难题分解为一组具有以下性质的子问题来克服它： •  

• 子问题比原问题更容易解决

• 可以组合子问题的解来解决原问题。

分而治之是一个非常古老的想法。 朱利叶斯·凯撒实行罗马人所说的分治（divide et impera）（分而治之）。 英国人在控制印度次大陆方面表现出色。 本杰明·富兰克林非常了解英国在使用这种技术方面的专业知识，促使他在签署美国独立宣言时说：“我们必须团结在一起，否则我们肯定会分开。” 在这种情况下，我们通过将原始问题分解为同一问题的更简单版本（检查较短的字符串是否为回文）和我们知道如何做的简单事情（比较单个字符）来解决问题，然后将 解决方案和。 图 4.9 包含一些可用于可视化其工作原理的代码。

```python
def isPalindrome(s):
   """Assumes s is a str
      Returns True if s is a palindrome; False otherwise.
        Punctuation marks, blanks, and capitalization are ignored."""
 def toChars(s):
   s = s.lower()
   letters = ''
   for c in s:
     if c in 'abcdefghijklmnopqrstuvwxyz':
       letters = letters + c
   return letters
 def isPal(s):
   print(' isPal called with', s)
   if len(s) <= 1:
      print(' About to return True from base case')
      return True
   else:
      answer = s[0] == s[-1] and isPal(s[1:-1])
      print(' About to return', answer, 'for', s)
      return answer
 return isPal(toChars(s))
def testIsPalindrome():
   print('Try dogGod')
   print(isPalindrome('dogGod'))
   print('Try doGood')
   print(isPalindrome('doGood'))
```

## 4.4 Global Variables

如果您尝试使用大数字调用 fib，您可能会注意到运行时间很长。 假设我们想知道进行了多少次递归调用？ 我们可以仔细分析代码并弄清楚，在第 9 章中我们将讨论如何做到这一点。 另一种方法是添加一些计算调用次数的代码。 一种方法是使用全局变量。

到目前为止，我们编写的所有函数都仅通过它们的参数和返回值与它们的环境进行通信。 在大多数情况下，这正是它应该的样子。 它通常会导致程序相对容易阅读、测试和调试。 然而，每隔一段时间，全局变量就会派上用场。 考虑图 4.10 中的代码。

在每个函数中，代码行全局 numFibCalls 告诉 Python 名称 numCalls 应该定义在代码行出现的模块的最外层范围（参见第 4.5 节），而不是在该行出现的函数范围内 代码出现。 如果我们不包括代码全局 numFibCalls，则名称 numFibCalls 将是 fib 和 testFib 函数的局部名称，因为 numFibCalls 出现在 fib 和 testFib 中赋值语句的左侧。 函数 fib 和 testFib 都可以不受限制地访问变量 numFibCalls 引用的对象。 函数 testFib 每次调用 fib 时将 numFibCalls 绑定为 0，fib 在每次调用 fib 时都会增加 numFibCalls 的值

```python
def fib(x):
   """Assumes x an int >= 0
      Returns Fibonacci of x"""
   global numFibCalls
   numFibCalls += 1
   if x == 0 or x == 1:
        return 1
   else:
        return fib(x-1) + fib(x-2)
def testFib(n):
   for i in range(n+1):
      global numFibCalls
      numFibCalls = 0
      print('fib of', i, '=', fib(i))
      print('fib called', numFibCalls, 'times.')
```

调用 testFib(6) 产生输出

```python
fib of 0 = 1
fib called 1 times.
fib of 1 = 1
fib called 1 times.
fib of 2 = 2
fib called 3 times.
fib of 3 = 3
fib called 5 times.
fib of 4 = 5
fib called 9 times.
fib of 5 = 8
fib called 15 times.
fib of 6 = 13
fib called 25 times.
```

引入全局变量的话题是带着些许不安的。自 1970 年代以来，持卡的计算机科学家一直在反对它们。不加选择地使用全局变量会导致很多问题。 使程序可读的关键是局部性。 一个人一次读一段程序，理解每一段所需的上下文越少越好。 由于全局变量可以在很多地方被修改或读取，因此草率地使用它们会破坏局部性。 然而，有时它们正是所需要的。

## 4.5 Modules

到目前为止，我们一直在假设我们的整个程序都存储在一个文件中进行操作。 只要程序很小，这是完全合理的。 然而，随着程序变得越来越大，将它们的不同部分存储在不同的文件中通常会更方便。 例如，想象一下，多个人在同一个程序上工作。 如果他们都试图更新同一个文件，那将是一场噩梦。  Python 模块使我们能够轻松地从多个文件中的代码构建程序。

模块是包含 Python 定义和语句的 .py 文件。 例如，我们可以创建一个包含图 4.11 中代码的文件 circle.py。

```python
pi = 3.14159
def area(radius):
   return pi*(radius**2)
def circumference(radius):
   return 2*pi*radius
def sphereSurface(radius):
   return 4.0*area(radius)
def sphereVolume(radius):
   return (4.0/3.0)*pi*(radius**3)
```

程序通过 import 访问模块。 所以，例如，代码

```python
import circle
pi = 3
print(pi)
print(circle.pi)
print(circle.area(3))
print(circle.circumference(3))
print(circle.sphereSurface(3))
```

会输出

```python
3
3.14159
28.27431
18.849539999999998
113.09724
```

模块通常存储在单独的文件中。 每个模块都有自己的私有符号表。 因此，在 circle.py 中，我们以通常的方式访问对象（例如，pi 和 area）。 执行导入 M 会在导入出现的范围内为模块 M 创建一个绑定。 因此，在导入上下文中，我们使用点表示法来表示我们引用的是导入模块中定义的名称。例如，在 circle.py 之外，引用 pi 和 circle.pi 可以（在这种情况下可以） 指不同的对象。

乍一看，点符号的使用似乎很麻烦。 另一方面，当人们导入一个模块时，通常不知道在该模块的实现中可能使用了哪些本地名称。 使用点符号来完全限定名称可避免因意外名称冲突而被烧毁的可能性。 例如，在 circle 模块外执行赋值 pi = 3 不会改变 circle 模块内使用的 pi 值。

import 语句有一个变体，它允许导入程序在访问导入模块中定义的名称时省略模块名称。 执行 from M import * 语句会在当前范围内创建与 M 中定义的所有对象的绑定，但不会创建与 M 本身的绑定。 例如，代码

```python
from circle import *
print(pi)
print(circle.pi)
```

会先输出 3.14159，然后产生错误信息

```python
NameError: name 'circle' is not defined
```

一些 Python 程序员不赞成使用这种形式的导入，因为他们认为这会使代码更难阅读。

正如我们所见，模块可以包含可执行语句和函数定义。 通常，这些语句用于初始化模块。 因此，模块中的语句仅在第一次将模块导入程序时执行。 此外，每个解释器会话只导入一次模块。 如果您启动一个 shell，导入一个模块，然后更改该模块的内容，解释器仍将使用该模块的原始版本。 这可能会导致调试时出现令人费解的行为。 如有疑问，请启动一个新的 shell。

有许多有用的模块是标准 Python 库的一部分。例如，很少需要编写您自己的常见数学或字符串函数的实现。 这个库的描述可以在 http://docs.python.org/2/library/ 找到。

## 4.6 Files

每个计算机系统都使用文件来保存从一个计算到下一个计算的内容。  Python 提供了许多用于创建和访问文件的工具。 这里我们说明一些基本的。

每个操作系统（例如 Windows 和 MAC OS）都有自己的文件系统，用于创建和访问文件。  Python通过称为文件句柄的东西访问文件来实现操作系统独立性。 编码

```matlab
nameHandle = open('kids', 'w')
```

指示操作系统创建一个名为 kids 的文件，并返回该文件的文件句柄。  open 的参数 'w' 表示要打开文件进行写入。 下面的代码打开一个文件，使用write方法写入两行，然后关闭文件。 重要的是要记住在程序使用完毕后关闭文件。 否则，可能无法保存部分或全部写入。

```python
nameHandle = open('kids', 'w')
for i in range(2):
    name = input('Enter name: ')
    nameHandle.write(name + '\n')
nameHandle.close()
```

在 Python 字符串中，转义字符“\”用于指示应以特殊方式处理下一个字符。 在此示例中，字符串 '\n' 表示换行符。

我们现在可以打开文件进行读取（使用参数“r”），并打印其内容。 由于 Python 将文件视为一系列行，因此我们可以使用 for 语句遍历文件的内容。

```python
nameHandle = open('kids', 'r')
for line in nameHandle:
  print(line)
nameHandle.close()
```

如果我们输入了 David 和 Andrea 的名字，这将输出

```python
David

Andrea
```

David 和 Andrea 之间有额外的一行，因为每次遇到文件中每一行末尾的 '\n' 时，print 都会开始一个新行。 我们本可以通过编写 print line[:-1] 来避免打印它。 编码

```python
nameHandle = open('kids', 'w')
nameHandle.write('Michael\n')
nameHandle.write('Mark\n')
nameHandle.close()
nameHandle = open('kids', 'r')
for line in nameHandle:
   print(line[:-1])
nameHandle.close()
```

将会输出

```python
Michael
Mark
```

请注意，我们已经覆盖了文件 kids.txt 的先前内容。 如果我们不想这样做，我们可以使用参数“a”打开文件进行追加（而不是写入）。 例如，如果我们现在运行代码

```python
nameHandle = open('kids', 'a')
nameHandle.write('David\n')
nameHandle.write('Andrea\n')
nameHandle.close()
nameHandle = open('kids', 'r')
for line in nameHandle:
   print(line[:-1])
nameHandle.close()
```

将会输出

```python
Michael
Mark
David
Andrea
```

open(fn, 'w') fn 是一个表示文件名的字符串。 创建一个用于写入的文件并返回一个文件句柄。

open(fn, 'r') fn 是一个表示文件名的字符串。 打开现有文件进行读取并返回文件句柄。

open(fn, 'a') fn 是一个表示文件名的字符串。 打开现有文件进行追加并返回文件句柄。

fh.read() 返回一个字符串，其中包含与文件句柄 fh 关联的文件的内容。

fh.readline() 返回文件中与文件句柄 fh 关联的下一行。

fh.readlines() 返回一个列表，其中每个元素都是与文件句柄 fh 关联的文件的一行。

fh.write(s) 将字符串 s 写入与文件句柄 fh 关联的文件末尾。

fh.writeLines(S) S 是一个字符串序列。 将 S 的每个元素作为单独的行写入与文件句柄 fh 关联的文件。

fh.close() 关闭与文件句柄 fh 关联的文件。

# 5 STRUCTURED TYPES, MUTABILITY, AND HIGHER-ORDER FUNCTIONS

到目前为止，我们看过的程序都处理了三种类型的对象：int、float 和 str。 数字类型 int 和 float 是标量类型。 也就是说，这些类型的对象没有可访问的内部结构。 相反， str 可以被认为是结构化的或非标量的类型。 可以使用索引从字符串中提取单个字符并使用切片来提取子字符串。

在本章中，我们介绍了四种额外的结构化类型。 一，元组，是 str 的一个相当简单的概括。 其他三个——list、range 和 dict——更有趣。 我们还通过一些示例返回函数的主题，这些示例说明了能够以与其他类型对象相同的方式处理函数的效用。

## 5.1 Tuples（元组）

像字符串一样，元组是不可变的有序元素序列。 不同之处在于元组的元素不必是字符。 各个元素可以是任何类型，并且不必彼此具有相同的类型。

元组类型的文字是通过将逗号分隔的元素列表括在括号内来编写的。 例如，我们可以写

```python
t1 = ()
t2 = (1, 'two', 3)
print(t1)
print(t2)
```

不出所料，打印语句产生输出

```python
()
(1, 'two', 3)
```

看看这个例子，你可能会自然而然地相信包含单个值 1 的元组会被写成 (1)。 但是，引用理查德尼克松的话，“那是错误的。” 由于括号用于对表达式进行分组，因此 (1) 只是写整数 1 的详细方式。为了表示包含该值的单例元组，我们写成 (1,)。 几乎每个使用 Python 的人都曾不小心遗漏了那个烦人的逗号。

重复可用于元组。 例如，表达式 3*('a', 2) 的计算结果为 ('a', 2, 'a', 2, 'a', 2)。

像字符串一样，元组可以连接、索引和切片。 考虑

```python
t1 = (1, 'two', 3)
t2 = (t1, 3.25)
print(t2)
print((t1 + t2))
print((t1 + t2)[3])
print((t1 + t2)[2:5])
```

第二个赋值语句将名称 t2 绑定到一个元组，该元组包含绑定 t1 的元组和浮点数 3.25。 这是可能的，因为元组与 Python 中的其他所有内容一样，是一个对象，因此元组可以包含元组。 因此，第一个打印语句产生输出

```python
((1, 'two', 3), 3.25)
```

第二个打印语句打印通过连接绑定到 t1 和 t2 的值生成的值，这是一个包含五个元素的元组。 它产生输出

```python
(1, 'two', 3, (1, 'two', 3), 3.25)
```

下一个语句选择并打印连接元组的第四个元素（在 Python 中，索引从 0 开始），之后的语句创建并打印该元组的切片，产生输出

```python
(1, 'two', 3)
(3, (1, 'two', 3), 3.25)
```

for 语句可用于迭代元组的元素：

```python
def intersect(t1, t2):
    """Assumes t1 and t2 are tuples
       Returns a tuple containing elements that are in
       both t1 and t2"""
    result = ()
    for e in t1:
       if e in t2:
          result += (e,)
    return result
```

### 5.1.1 Sequences and Multiple Assignment

如果您知道序列的长度（例如，元组或字符串），则可以方便地使用 Python 的多重赋值语句来提取单个元素。例如，执行语句 x, y = (3, 4) 后，x 将绑定到 3，y 将绑定到 4。类似地，语句 a, b, c = 'xyz' 将 a 绑定到 'x', b 到 'y'，c 到 'z'。

当与返回固定大小序列的函数结合使用时，这种机制特别方便。 考虑，例如函数定义 

```python
def findExtremeDivisors(n1, n2):
  """Assumes that n1 and n2 are positive ints
     Returns a tuple containing the smallest common divisor > 1        and the largest common divisor of n1 and n2. If no common          divisor,returns (None, None)"""
    minVal, maxVal = None, None
    for i in range(2, min(n1, n2) + 1):
       if n1%i == 0 and n2%i == 0:
         if minVal == None:
               minVal = i
          maxVal = i
    return (minVal, maxVal)
```

多重赋值语句

```python
minDivisor, maxDivisor = findExtremeDivisors(100, 200)
```

将 minDivisor 绑定到 2 并将 maxDivisor 绑定到 100。

## 5.2 Ranges

像字符串和元组一样，范围是不可变的。  range 函数返回一个范围类型的对象。 如 3.2 节所述，range 函数接受三个整数参数：`start、stop` 和 step，并返回整数 `start、start + step、start + 2*step` 等的级数。如果 step 为正数，则最后一个元素为 最大整数 `start + i*step` 小于 stop。 如果 step 为负数，则最后一个元素是大于 stop 的最小整数 `start + i*step`。 如果仅提供两个参数，则使用步长 1。 如果只提供一个参数，则该参数是停止，开始默认为 0，步骤默认为 1。

除了串联和重复之外，元组上的所有操作也可用于范围。 例如， `range(10)[2:6][2]` 的计算结果为 4。当 == 运算符用于比较 range 类型的对象时，如果两个范围表示相同的整数序列，则返回 True。 例如， `range(0, 7, 2) == range(0, 8, 2)` 的计算结果为 True。 但是， `range(0, 7, 2) == range(6, -1, -2)` 的计算结果为 False，因为尽管这两个范围包含相同的整数，但它们以不同的顺序出现。

与 tuple 类型的对象不同，range 类型的对象占用的空间量与其长度不成正比。 因为范围完全由其开始、停止和步长值定义； 它可以存储在很小的空间内。

range 最常见的用途是在 for 循环中，但是 range 类型的对象可以用于任何可以使用整数序列的地方。

## 5.3 Lists and Mutability（列表和可变性）

像元组一样，列表是一个有序的值序列，其中每个值都由一个索引标识。 表达类型列表文字的语法类似于元组使用的语法； 不同之处在于我们使用方括号而不是圆括号。空列表写为 []，单例列表在右括号前没有逗号（哦，很容易忘记）。 所以，例如，代码，

```python
L = ['I did it all', 4, 'love']
for i in range(len(L)):
   print(L[i])
```

会产生输出

```python
I did it all
4
love
```

有时，方括号用于列表类型的文字、索引到列表和切片列表的事实可能会导致一些视觉混乱。 例如，计算结果为 3 的表达式 `[1,2,3,4][1:3][1]` 以三种不同的方式使用方括号。 这在实践中很少成为问题，因为大多数时间列表都是增量构建的，而不是写成文字。

列表在一个非常重要的方面不同于元组：列表是可变的。 相比之下，元组和字符串是不可变的。 有很多操作符可以用来创建这些不可变类型的对象，变量可以绑定到这些类型的对象上。 但是不能修改不可变类型的对象。 另一方面，列表类型的对象可以在创建后进行修改。

改变对象和将对象分配给变量之间的区别乍一看似乎很微妙。 但是，如果您不断重复这句口头禅，“在 Python 中，变量只是一个名称，即可以附加到对象的标签”，它会让您变得清晰。

当陈述

```python
Techs = ['MIT', 'Caltech']
Ivys = ['Harvard', 'Yale', 'Brown']
```

执行时，解释器创建两个新列表并将适当的变量绑定到它们，如图 5.1 所示。

<img src="C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210831145510762.png" alt="image-20210831145510762" style="zoom: 67%;" />

赋值语句

```python
Univs = [Techs, Ivys]
Univs1 = [['MIT', 'Caltech'], ['Harvard', 'Yale', 'Brown']]
```

还创建新列表并将变量绑定到它们。 这些列表的元素本身就是列表。 三个打印语句

```python
print('Univs =', Univs)
print('Univs1 =', Univs1)
print(Univs == Univs1)
```

产生输出

```python
Univs = [['MIT', 'Caltech'], ['Harvard', 'Yale', 'Brown']]
Univs1 = [['MIT', 'Caltech'], ['Harvard', 'Yale', 'Brown']]
True
```

看起来好像 Univs 和 Univs1 绑定到相同的值。 但外表可能是骗人的。 如图 5.2 所示，Univs 和 Univs1 绑定到完全不同的值。

<img src="C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210831145739047.png" alt="image-20210831145739047" style="zoom: 67%;" />

可以使用内置的 Python 函数 id 验证 Univs 和 Univs1 绑定到不同的对象，该函数返回对象的唯一整数标识符。这个函数允许我们测试对象是否相同。 当我们运行代码 

```python
print(Univs == Univs1) #test value equality
print(id(Univs) == id(Univs1)) #test object equality
print('Id of Univs =', id(Univs))
print('Id of Univs1 =', id(Univs1))
```

将会输出

```python
True
False
Id of Univs = 4447805768
Id of Univs1 = 4456134408
```

（如果你运行这段代码，不要期望看到相同的唯一标识符。Python 的语义没有说明每个对象关联什么标识符；它只要求没有两个对象具有相同的标识符。）注意图 5.2 中的 Univs 的元素不是 Techs 和 Ivys 所绑定的列表的副本，而是列表本身。  Univs1 的元素是包含与 Univs 中的列表相同元素的列表，但它们不是相同的列表。 我们可以通过运行代码看到这一点

```python
print('Ids of Univs[0] and Univs[1]', id(Univs[0]), id(Univs[1]))
print('Ids of Univs1[0] and Univs1[1]', id(Univs1[0]), id(Univs1[1]))
```

将会输出

```python
Ids of Univs[0] and Univs[1] 4447807688 4456134664
Ids of Univs1[0] and Univs1[1] 4447805768 4447806728
```

为什么这很重要？ 这很重要，因为列表是可变的。 考虑代码

```python
Techs.append('RPI')
```

append 方法有副作用。 它不是创建一个新列表，而是通过在其末尾添加一个新元素（字符串“RPI”）来改变现有列表 Techs。 图 5.3 描述了执行 append 后的计算状态

<img src="C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210831150201815.png" alt="image-20210831150201815" style="zoom:67%;" />

图 5.3 可变性演示

Univs 绑定到的对象仍然包含相同的两个列表，但其中一个列表的内容已更改。 因此，打印语句

```python
print('Univs =', Univs)
print('Univs1 =', Univs1)
```

现在产生输出

```python
Univs = [['MIT', 'Caltech', 'RPI'], ['Harvard', 'Yale', 'Brown']]
Univs1 = [['MIT', 'Caltech'], ['Harvard', 'Yale', 'Brown']]
```

我们这里有一种叫做混叠的东西。 同一个列表对象有两条不同的路径。 一条路径是通过变量 Techs，另一条路径是通过 Univs 绑定到的列表对象的第一个元素。 可以通过任一路径对对象进行变异，并且通过这两条路径都可以看到变异的效果。 这可能很方便，但也可能很危险。 无意的混叠会导致编程错误，而这些错误通常很难追踪。

与元组一样，for 语句可用于迭代列表的元素。 例如，

```python
for e in Univs:
  print('Univs contains', e)
  print(' which contains')
  for u in e:
     print(' ', u)
```

将会输出

```python
Univs contains ['MIT', 'Caltech', 'RPI']
 which contains
   MIT
   Caltech
   RPI
Univs contains ['Harvard', 'Yale', 'Brown']
 which contains
   Harvard
   Yale
   Brown
```

当我们将一个列表附加到另一个列表时，例如 Techs.append(Ivys)，原始结构将保持不变。 即，结果是一个包含列表的列表。 假设我们不想维护这种结构，而是想将一个列表的元素添加到另一个列表中。 我们可以通过使用列表连接或扩展方法来做到这一点，例如，

```python
L1 = [1,2,3]
L2 = [4,5,6]
L3 = L1 + L2
print('L3 =', L3)
L1.extend(L2)
print('L1 =', L1)
L1.append(L2)
print('L1 =', L1)
```

将会输出

```python
L3 = [1, 2, 3, 4, 5, 6]
L1 = [1, 2, 3, 4, 5, 6]
L1 = [1, 2, 3, 4, 5, 6, [4, 5, 6]]
```

请注意，运算符 + 没有副作用。 它创建一个新列表并返回它。 相比之下，扩展和附加每个突变的 L1。

图 5.4 包含一些与列表相关的方法的简短描述。 请注意，除了 count 和 index 之外的所有这些都会改变列表。

L.append(e) 将对象 e 添加到 L 的末尾。

L.count(e) 返回 e 在 L 中出现的次数。

L.insert(i, e) 在索引 i 处将对象 e 插入到 L 中。

L.extend(L1) 将列表 L1 中的项目添加到 L 的末尾。

L.remove(e) 从 L 中删除第一次出现的 e。

L.index(e) 返回 e 在 L 中第一次出现的索引，如果 e 不在 L 中，则引发异常（参见第 7 章）。

L.pop(i) 删除并返回 L 中索引 i 处的项目，如果 L 为空则引发异常。 如果省略 i，则默认为 -1，以删除并返回 L 的最后一个元素。

L.sort() 按升序对 L 的元素进行排序。

L.reverse() 反转 L 中元素的顺序。

### 5.3.1 Cloning

通常谨慎的做法是避免改变正在迭代的列表。 例如，考虑代码

```python
def removeDups(L1, L2):
    """Assumes that L1 and L2 are lists.
       Removes any element from L1 that also occurs in L2"""
    for e1 in L1:
       if e1 in L2:
          L1.remove(e1)
L1 = [1,2,3,4]
L2 = [1,2,5,6]
removeDups(L1, L2)
print('L1 =', L1)
```

你可能会惊讶地发现这会输出

```python
L1 = [2, 3, 4]
```

在 for 循环期间，Python 的实现使用在每次迭代结束时递增的内部计数器来跟踪它在列表中的位置。当计数器的值达到列表的当前长度时，循环终止。 如果列表在循环中没有发生变异，这可能会像人们预期的那样工作，但如果列表发生变异，则会产生令人惊讶的后果。 在这种情况下，隐藏计数器从 0 开始，发现 L1[0] 在 L2 中，并将其删除——将 L1 的长度减少到 3。然后计数器增加到 1，代码继续检查是否 L1[1] 的值在 L2 中。 **请注意，这不是 L1[1] 的原始值（即 2），而是 L1[1] 的当前值（即 3）**。 如您所见，可以弄清楚在循环内修改列表时会发生什么。 然而，这并不容易。 发生的事情很可能是无意的，如本例所示。

避免此类问题的一种方法是使用切片来克隆（即复制）列表并在 L1[:] 中写入 e1。 注意写

```python
newL1 = L1
for e1 in newL1:
```

不会解决问题。 它不会创建 L1 的副本，而只会为现有列表引入一个新名称。

切片并不是在 Python 中克隆列表的唯一方法。 表达式 list(L) 返回列表 L 的副本。如果要复制的列表包含您也想复制的可变对象，请导入标准库模块 copy 并使用函数 copy.deepcopy。

### 5.3.2 List Comprehension

列表推导式提供了一种对序列中的值应用操作的简洁方法。 它创建一个新列表，其中每个元素都是将给定操作应用于序列中的值（例如，另一个列表中的元素）的结果。 例如，

```python
L = [x**2 for x in range(1,7)]
print(L)
```

将会输出

```python
[1, 4, 9, 16, 25, 36]
```

列表推导式中的 for 子句后面可以跟一个或多个 if 和 for 语句，这些语句应用于 for 子句生成的值。 这些附加子句修改由第一个 for 子句生成的值序列，并产生一个新的值序列，与推导相关的操作应用于该序列。 例如，代码

```python
mixed = [1, 2, 'a', 3, 4.0]
print([x**2 for x in mixed if type(x) == int])
```

对混合中的整数进行平方，然后打印 [1, 4, 9]。

一些 Python 程序员以奇妙而微妙的方式使用列表推导式。 这并不总是一个好主意。 请记住，其他人可能需要阅读您的代码，而“微妙”通常不是理想的属性。

## 5.4 Functions as Objects

在 Python 中，函数是一等对象。 这意味着它们可以被视为任何其他类型的对象，例如 int 或 list。 它们有类型，例如，表达式 type(abs) 的值是 <type 'built-in_function_or_method'>; 它们可以出现在表达式中，例如，作为赋值语句的右侧或作为函数的参数； 它们可以是列表的元素； 等等。

使用函数作为参数允许一种称为高阶编程的编码风格。 结合列表可以特别方便，如图5.5

```python
def applyToEach(L, f):
    """Assumes L is a list, f a function
       Mutates L by replacing each element, e, of L by f(e)"""
    for i in range(len(L)):
       L[i] = f(L[i])

L = [1, -2, 3.33]
print('L =', L)
print('Apply abs to each element of L.')
applyToEach(L, abs)
print('L =', L)
print('Apply int to each element of', L)
applyToEach(L, int)
print('L =', L)
print('Apply factorial to each element of', L)
applyToEach(L, factR)
print('L =', L)
print('Apply Fibonnaci to each element of', L)
applyToEach(L, fib)
print('L =', L)
```

函数 applyToEach 被称为高阶函数，因为它有一个参数本身就是一个函数。 第一次调用时，它通过将一元内置函数 abs 应用于每个元素来改变 L。 第二次调用时，它对每个元素应用类型转换。 第三次调用它时，它通过将函数 factR（在图 4.5 中定义）应用于每个元素的结果替换每个元素。 第四次调用它时，它通过将函数 fib（在图 4.7 中定义）应用于每个元素的结果替换每个元素。 它打印

```python
L = [1, -2, 3.33]
Apply abs to each element of L.
L = [1, 2, 3.33]
Apply int to each element of [1, 2, 3.33]
L = [1, 2, 3]
Apply factorial to each element of [1, 2, 3]
L = [1, 2, 6]
Apply Fibonnaci to each element of [1, 2, 6]
L = [1, 2, 13]
```

Python 有一个内置的高阶函数 map，它类似于图 5.5 中定义的 applyToEach 函数，但比它更通用。 它旨在与 for 循环结合使用。 在最简单的形式中，map 的第一个参数是一个一元函数（即只有一个参数的函数），第二个参数是任何适合作为第一个参数的参数的有序值集合。

在 for 循环中使用时，map 的行为类似于 range 函数，因为它为循环的每次迭代返回一个值。这些值是通过将第一个参数应用于第二个参数的每个元素而生成的。 例如，代码

```python
for i in map(fib, [2, 6, 4]):
   print(i)
```

将会输出

```python
2
13
5
```

更一般地，map 的第一个参数可以是一个包含 n 个参数的函数，在这种情况下，它后面必须跟有 n 个后续有序集合（每个长度相同）。 例如，代码

```python
L1 = [1, 28, 36]
L2 = [2, 57, 9]
for i in map(min, L1, L2):
    print(i)
```

将会输出

```python
1
28
9
```

Python 支持使用保留字 lambda 创建匿名函数（即未绑定到名称的函数）。 lambda 表达式的一般形式是

```python
lambda <sequence of variable names>: <expression>
```

例如，lambda 表达式 lambda x, y: x*y 返回一个函数，该函数返回其两个参数的乘积。  Lambda 表达式经常用作高阶函数的参数。 例如，代码

```python
 L = []
 for i in map(lambda x, y: x**y, [1 ,2 ,3, 4], [3, 2, 1, 0]):
     L.append(i)
 print(L)
prints [1, 4, 3, 1].
```

## 5.5 Strings, Tuples, Ranges, and List

我们已经研究了四种不同的序列类型：str、tuple、range 和 list。 它们的相似之处在于可以对这些类型的对象进行操作，如图 5.6 所示。 图 5.7 总结了它们的一些其他异同。

seq[i] 返回序列中的第 i 个元素。

len(seq) 返回序列的长度。

seq1 + seq2 返回两个序列的串联（不适用于范围）。

n*seq 返回一个重复 seq n 次的序列（不适用于范围）。

seq[start:end] 返回序列的一个切片。

如果 e 包含在序列中，则 e in seq 为 True，否则为 False。

如果 e 不在序列中，则 e not in seq 为 True，否则为 False。

for e in seq 迭代序列的元素。

<img src="C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210831160931770.png" alt="image-20210831160931770" style="zoom: 67%;" />

Python 程序员往往比元组更频繁地使用列表。 由于列表是可变的，它们可以在计算过程中增量构建。 例如，以下代码逐步构建一个列表，其中包含另一个列表中的所有偶数。

```python
evenElems = []
for e in L:
    if e%2 == 0:
       evenElems.append(e)
```

元组的一个优点是因为它们是不可变的，所以不必担心别名。 它们不可变的另一个优点是，与列表不同，元组可以用作字典中的键，我们将在下一节中看到。

由于字符串只能包含字符，因此它们的通用性远不如元组或列表。 另一方面，当您处理一串字符时，有许多内置方法可以使生活变得轻松。 图 5.8 包含其中一些的简短描述。 请记住，由于字符串是不可变的，因此这些所有返回值都没有副作用。

更有用的内置方法之一是 split，它接受两个字符串作为参数。 第二个参数指定一个分隔符，用于将第一个参数拆分为子字符串序列。 例如，

```python
print('My favorite professor--John G.--rocks'.split(' '))
print('My favorite professor--John G.--rocks'.split('-'))
print('My favorite professor--John G.--rocks'.split('--'))
```

输出

```python
['My', 'favorite', 'professor--John', 'G.--rocks']
['My favorite professor', '', 'John G.', '', 'rocks']
['My favorite professor', 'John G.', 'rocks']
```

第二个参数是可选的。 如果省略该参数，则使用任意空白字符字符串（空格、制表符、换行符、回车符和换页符）拆分第一个字符串。

s.count(s1) 计算字符串 s1 在 s 中出现的次数。

s.find(s1) 返回子字符串 s1 在 s 中第一次出现的索引，如果 s1 不在 s 中，则返回 -1。

s.rfind(s1) 与 find 相同，但从 s 的末尾开始（rfind 中的“r”代表反向）。

s.index(s1) 与 find 相同，但如果 s1 不在 s 中，则会引发异常（第 7 章）。

s.rindex(s1) 与 index 相同，但从 s 的末尾开始。

s.lower() 将 s 中的所有大写字母转换为小写。

s.replace(old, new) 用字符串 new 替换 s 中所有出现的字符串 old 。

s.rstrip() 从 s 中删除尾随空格。

s.split(d) 使用 d 作为分隔符拆分 s。 返回 s 的子字符串列表。 例如，'David Guttag 打篮球'.split(' ') 的值是 ['David', 'Guttag', 'plays', 'basketball']。 如果省略 d，则子字符串由任意的空白字符字符串分隔

## 5.6 Dictionaries

dict（dictionary 的缩写）类型的对象类似于列表，只是我们使用键对其进行索引。 将字典视为一组键/值对。  dict 类型的文字用大括号括起来，每个元素都写成一个键，后跟一个冒号，后跟一个值。 例如，代码，

```python
monthNumbers = {'Jan':1, 'Feb':2, 'Mar':3, 'Apr':4, 'May':5,
1:'Jan', 2:'Feb', 3:'Mar', 4:'Apr', 5:'May'}
print('The third month is ' + monthNumbers[3])
dist = monthNumbers['Apr'] - monthNumbers['Jan']
print('Apr and Jan are', dist, 'months apart')
```

将会输出

```python
The third month is Mar
Apr and Jan are 3 months apart
```

dict 中的条目是无序的，不能用索引访问。这就是为什么 monthNumbers[1] 明确引用键为 1 的条目而不是第二个条目的原因。

和列表一样，字典也是可变的。 我们可以通过写来添加一个条目

```python
monthNumbers['June'] = 6
```

或通过写入更改条目

```python
monthNumbers['May'] = 'V'
```

字典是 Python 的一大优点。 它们大大降低了编写各种程序的难度。 例如，在图 5.9 中，我们使用字典编写了一个（非常可怕的）程序来在语言之间进行翻译。由于其中一行代码太长而无法在页面上显示，我们使用反斜杠 \ 来指示下一行文本是前一行的延续。

```python
EtoF = {'bread':'pain', 'wine':'vin', 'with':'avec', 'I':'Je',
'eat':'mange', 'drink':'bois', 'John':'Jean',
'friends':'amis', 'and': 'et', 'of':'du','red':'rouge'}
FtoE = {'pain':'bread', 'vin':'wine', 'avec':'with', 'Je':'I',
'mange':'eat', 'bois':'drink', 'Jean':'John',
'amis':'friends', 'et':'and', 'du':'of', 'rouge':'red'}
dicts = {'English to French':EtoF, 'French to English':FtoE}
def translateWord(word, dictionary):
    if word in dictionary.keys():
         return dictionary[word]
    elif word != '':
         return '"' + word + '"'
    return word
def translate(phrase, dicts, direction):
    UCLetters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
    LCLetters = 'abcdefghijklmnopqrstuvwxyz'
    letters = UCLetters + LCLetters
    dictionary = dicts[direction]
    translation = ''
    word = ''
    for c in phrase:
        if c in letters:
           word = word + c
        else:
           translation = translation\
                   + translateWord(word, dictionary) + c
           word = ''
    return translation + ' ' + translateWord(word, dictionary)
print(translate('I drink good red wine, and eat bread.',dicts,'English to French'))
print(translate('Je bois du vin rouge.',dicts, 'French to English'))
```

图中的代码打印， 

```python
Je bois "good" rouge vin, et mange pain.
I drink of wine red.
```

请记住，字典是可变的。 所以一定要注意副作用。 例如，

```python
FtoE['bois'] = 'wood'
Print(translate('Je bois du vin rouge.', dicts, 'French to English'))
```

会输出

```python
I wood of wine red
```

大多数编程语言不包含提供从键到值的映射的内置类型。 相反，程序员使用其他类型来提供类似的功能。 例如，通过使用每个元素是一个键/值对的列表来实现字典是相对容易的。 然后可以编写一个简单的函数来进行关联检索，例如，

```python
def keySearch(L, k):
    for elem in L:
        if elem[0] == k:
           return elem[1]
    return None
```

这种实现的问题在于它的计算效率低下。在最坏的情况下，程序可能必须检查列表中的每个元素才能执行一次检索。 相比之下，内置的实现速度相当快。 它使用一种称为散列的技术，在第 10 章中进行了描述，以在时间上进行查找，这几乎与字典的大小无关。

for 语句可用于迭代字典中的条目。 但是，分配给迭代变量的值是键，而不是键/值对。 没有定义在迭代中看到键的顺序。 例如，代码

```python
monthNumbers = {'Jan':1, 'Feb':2, 'Mar':3, 'Apr':4, 'May':5,
                1:'Jan', 2:'Feb', 3:'Mar', 4:'Apr', 5:'May'}
keys = []
for e in monthNumbers:
    keys.append(str(e))
print(keys)
keys.sort()
print(keys）
```

可能会输出

```python
['Jan', 'Mar', '2', '3', '4', '5', '1', 'Feb', 'May', 'Apr']
['1', '2', '3', '4', '5', 'Apr', 'Feb', 'Jan', 'Mar', 'May']
```

方法keys 返回一个dict_keys 类型的对象。这是一个视图对象的例子。 键在视图中出现的顺序没有定义。 视图对象是动态的，因为如果与其关联的对象发生变化，则该变化通过视图对象可见。 例如

```python
birthStones = {'Jan':'Garnet', 'Feb':'Amethyst',                                  'Mar':'Acquamarine','Apr':'Diamond', 'May':'Emerald'}
months = birthStones.keys()
print(months)
birthStones['June'] = 'Pearl'
print(months)
```

可能会输出

```python
dict_keys(['Jan', 'Feb', 'May', 'Apr', 'Mar'])
dict_keys(['Jan', 'Mar', 'June', 'Feb', 'May', 'Apr'])
```

dict_keys 类型的对象可以使用 for 进行迭代，成员资格可以使用 in 进行测试。 dict_keys 类型的对象可以很容易地转换为列表，例如 list(months)。

并非所有类型的对象都可以用作键：键必须是可散列类型的对象。 一个类型是可散列的，如果它有

•一个 __hash__ 方法将类型的对象映射到 int，对于每个对象，__hash__ 返回的值在对象的生命周期内不会改变，并且 

• 一个__eq__ 方法用于比较对象是否相等。

Python 的所有内置不可变类型都是可散列的，而 Python 的所有内置可变类型都不是可散列的。 使用元组作为键通常很方便。

例如，想象一下，使用形式为 (flightNumber, day) 的元组来表示航空公司航班。 然后很容易使用这样的元组作为字典中的键，实现从航班到到达时间的映射。

与列表一样，有许多与字典相关的有用方法，包括一些用于删除元素的方法。 我们在此不一一列举，但会在本书后面的示例中方便地使用它们。 图 5.10 包含了一些对字典更有用的操作

len(d) 返回 d 中的项目数。

d.keys() 返回 d 中键的视图。

d.values() 返回 d 中值的视图。

如果键 k 在 d 中，则 k in d 返回 True。

d[k] 返回 d 中键为 k 的项目。

如果 k 在 d 中，则 d.get(k, v) 返回 d[k]，否则返回 v。

d[k] = v 将值 v 与 d 中的键 k 相关联。 如果已经存在与 k 关联的值，则替换该值。

del d[k] 从 d 中删除键 k。

for k in d 迭代 d 中的键。

# 6 TESTING AND DEBUGGING

我们不想提起这个，但 Pangloss 博士错了。 我们并不生活在“所有可能世界中最好的世界”。 有些地方下雨太少，有些地方下雨太多。 有的地方太冷，有的地方太热，有的地方夏天太热，冬天太冷。 有时股市会下跌——很多。 而且，令人讨厌的是，我们的程序在我们第一次运行时并不总是正常运行。

关于如何处理最后一个问题的书已经写了，从阅读这些书中可以学到很多东西。 但是，为了向您提供一些提示以帮助您及时解决下一个问题，本章提供了对该主题的高度浓缩的讨论。 虽然所有的编程示例都是用 Python 编写的，但一般原则适用于让任何复杂系统工作。

测试是运行程序以尝试确定它是否按预期工作的过程。 调试是尝试修复您已经知道无法按预期工作的程序的过程。

测试和调试不是您应该在构建程序后开始考虑的过程。 优秀的程序员以更易于测试和调试的方式设计他们的程序。 这样做的关键是将程序分解成独立的组件，这些组件可以独立于其他组件来实现、测试和调试。 在本书的这一点上，我们只讨论了一种模块化程序的机制，即函数。因此，就目前而言，我们所有的示例都将基于函数。 当我们谈到其他机制，特别是类时，我们将回到本章中涉及的一些主题。

让程序运行的第一步是让语言系统同意运行它——也就是说，消除无需运行程序即可检测到的语法错误和静态语义错误。 如果您在编程中还没有超过这一点，那么您还没有为本章做好准备。 多花一点时间在小程序上，然后再回来。

## 6.1 Testing

关于测试最重要的一点是，它的目的是表明存在错误，而不是表明程序没有错误。 引用 Edsger Dijkstra 的话，“程序测试可以用来显示错误的存在，但绝不能显示错误的存在！”或者，正如阿尔伯特·爱因斯坦所说，“再多的实验也无法证明我是正确的； 一个实验就可以证明我是错的。” 

为什么会这样？ 即使是最简单的程序也有数十亿个可能的输入。例如，考虑一个声称满足规范的程序

```python
def isBigger(x, y):
    """Assumes x and y are ints
       Returns True if x is less than y and False otherwise."""
```

在所有整数对上运行它，至少可以说是乏味的。 我们能做的最好的事情是在成对的整数上运行它，如果程序中存在错误，这些整数对很可能会产生错误的答案。

测试的关键是找到一组输入，称为测试套件，它很有可能揭示错误，但运行时间不会太长。 这样做的关键是将所有可能输入的空间划分为子集，这些子集提供有关程序正确性的等效信息，然后构建一个测试套件，其中包含来自每个分区的至少一个输入。  （通常，构建这样的测试套件实际上是不可能的。可以将其视为无法实现的理想。）

集合的分区将集合划分为子集的集合，使得原始集合的每个元素都恰好属于其中一个子集 . 例如，考虑 isBigger(x, y)。 可能输入的集合都是整数的成对组合。 将这个集合划分为这七个子集的一种方法是：

x正，y正 

x负，y负 

x正，y负 

x负，y正

```python
x = 0, y = 0 x = 0, y ≠ 0 x ≠ 0, y = 0
```

如果对每个这些子集中的至少一个值测试了实现，那么如果存在错误，就会有合理的概率（但不能保证）暴露错误。

对于大多数程序来说，找到一个好的输入分区说起来容易做起来难。 通常，人们依赖基于通过代码和规范的某种组合探索不同路径的启发式方法。 基于启发式

### 6.1.1 Black-Box Testing

原则上，黑盒测试是在不查看要测试的代码的情况下构建的。 黑盒测试允许测试人员和实施人员来自不同的人群。 当我们这些教授编程课程的人为我们分配给学生的问题集生成测试用例时，我们正在开发黑盒测试套件。 商业软件的开发人员通常拥有很大程度上独立于开发团队的质量保证团队。

这种独立性降低了生成出现与代码错误相关的错误的测试套件的可能性。 例如，假设一个程序的作者做出了一个隐含但无效的假设，即永远不会用负数调用函数。 如果同一个人为程序构建了测试套件，他很可能会重复错误，并且不会使用否定参数来测试函数。

黑盒测试的另一个积极特征是它在实现更改方面是健壮的。 由于测试数据是在不了解实现的情况下生成的，因此在更改实现时不需要更改测试。正如我们之前所说，生成黑盒测试数据的一个好方法是通过规范探索路径。 考虑，规范

```python
def sqrt(x, epsilon):
    """Assumes x, epsilon floats
               x >= 0
               epsilon > 0
       Returns result such that
               x-epsilon <= result*result <= x+epsilon"""
```

通过这个规范似乎只有两条不同的路径：一条对应于 x = 0，一条对应于 x > 0。然而，常识告诉我们，虽然有必要测试这两种情况，但这还不够。

还应测试边界条件。 在查看列表时，这通常意味着查看空列表、只有一个元素的列表和包含列表的列表。 在处理数字时，它通常意味着查看非常小的和非常大的值以及“典型”值。 例如，对于 sqrt，尝试类似于图 6.1 中的 x 和 epsilon 值可能是有意义的。

前四行旨在代表典型案例。 请注意，x 的值包括一个完全平方数、一个小于 1 的数字和一个带有小数点的浮点数

<img src="C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210901155047801.png" alt="image-20210901155047801" style="zoom:67%;" />

其余行测试 x 和 epsilon 的极大值和极小值。 如果这些测试中的任何一个失败，则需要修复某些内容。 可能是代码中存在需要修复的错误，或者可能需要更改规范以便更容易满足。 例如，当 epsilon 小得离谱时，期望找到平方根的近似值可能是不合理的。

另一个需要考虑的重要边界条件是混叠。 例如，考虑代码

```python
def copy(L1, L2):
    """Assumes L1, L2 are lists
       Mutates L2 to be a copy of L1"""
    while len(L2) > 0: #remove all elements from L2
        L2.pop() #remove last element of L2
    for e in L1: #append L1's elements to initially empty L2
        L2.append(e)
```

它在大多数情况下都有效，但在 L1 和 L2 引用同一个列表时无效。 任何不包含 copy(L, L) 形式调用的测试套件都不会显示错误。

### 6.1.2 Glass-box Testing

永远不应该跳过黑盒测试，但它很少足够。 如果不查看代码的内部结构，就不可能知道哪些测试用例可能提供新信息。 考虑一个简单的例子：

```python
def isPrime(x):
    """Assumes x is a nonnegative int
       Returns True if x is prime; False otherwise"""
    if x <= 2:
       return False
    for i in range(2, x):
       if x%i == 0:
           return False
return True
```

查看代码，我们可以看到，由于测试 if x <= 2，值 0、1 和 2 被视为特殊情况，因此需要进行测试。 如果不看代码，人们可能不会测试 isPrime(2)，因此不会发现函数调用 isPrime(2) 返回 False，错误地表明 2 不是素数。

玻璃盒测试套件通常比黑盒测试套件更容易构建。 规范通常不完整，而且通常非常草率，这使得评估黑盒测试套件探索有趣输入空间的彻底程度成为一项挑战。 相比之下，代码路径的概念是明确定义的，评估一个人探索空间的彻底程度相对容易。
 事实上，有一些商业工具可以用来客观地衡量玻璃盒测试的完整性。

如果一个玻璃盒测试套件在程序中执行每一个潜在的路径，那么它就是路径完备的。 这通常是不可能实现的，因为它取决于每个循环的执行次数和每次递归的深度。

例如，对于每个可能的输入，阶乘的递归实现遵循不同的路径（因为递归级别的数量会有所不同）。

此外，即使是路径完整的测试套件也不能保证会暴露所有错误。 考虑 

```python
def abs(x):
    """Assumes x is an int
       Returns x if x>=0 and –x otherwise"""
    if x < -1:
        return -x
    else:
        return x
```

规范建议有两种可能的情况：x 要么是负数，要么不是。 这表明输入集 {2, -2} 足以探索规范中的所有路径。 该测试套件具有强制程序通过其所有路径的附加特性，因此它看起来也像一个完整的玻璃盒套件。 唯一的问题是这个测试套件不会暴露 abs(-1) 将返回 -1 的事实。

尽管玻璃盒测试存在局限性，但有一些经验法则通常值得遵循：

• 练习所有if 语句的两个分支。

• 确保每个except 子句（见第7 章）都得到执行。

• 对于每个 for 循环，有测试用例，其中 

o 没有进入循环（例如，如果循环迭代列表的元素，请确保它在空列表上进行测试）， 

o 循环体 只执行一次，并且 

o 循环体被执行多次。

• 对于每个while 循环， 

o 查看与处理for 循环时相同的情况。

o 包括与退出循环的所有可能方式相对应的测试用例。例如，对于以 while len(L) > 0 而不是 L[i] == e 开始的循环，查找循环因 len(L) 大于零而退出的情况以及因 L[i] == e 而退出的情况 = e。

• 对于递归函数，包括导致函数在没有递归调用、恰好一次递归调用和多次递归调用的情况下返回的测试用例。

### 6.1.3 Conducting Testsg

测试通常被认为分两个阶段进行。 应该始终从单元测试开始。 在此阶段，测试人员构建并运行旨在确定各个代码单元（例如，函数）是否正常工作的测试。 接下来是集成测试，旨在确定程序作为一个整体是否按预期运行。 在实践中，测试人员在这两个阶段循环，因为集成测试期间的失败会导致对单个单元进行更改。

集成测试几乎总是比单元测试更具挑战性。 一个原因是整个程序的预期行为通常比其每个部分的预期行为更难表征。 例如，表征文字处理器的预期行为比表征计算文档中字符数的函数的行为更具挑战性。 规模问题也会使集成测试变得困难。 运行集成测试需要数小时甚至数天的情况并不少见。

许多工业软件开发组织都有一个软件质量保证 (SQA) 小组，该小组独立于负责实施软件的小组。 该小组的任务是确保在软件发布之前它适合其预期用途。 在一些组织中，开发组负责单元测试，QA 组负责集成测试。

在工业中，测试过程通常是高度自动化的。 测试人员不会坐在终端输入输入和检查输出。 相反，他们使用自动测试驱动程序

• 设置调用要测试的程序（或单元）所需的环境， 

• 使用预定义的或自动生成的输入序列调用要测试的程序（或单元）， 

• 保存这些调用的结果， 

• 检查 测试结果的可接受性，以及 

• 准备一份适当的报告。

在单元测试期间，我们经常需要构建存根和驱动程序。 驱动程序模拟使用被测试单元的程序部分，而存根模拟被测试单元使用的程序部分。 存根很有用，因为它们允许人们测试依赖于软件或有时甚至尚不存在的硬件的单元。 这允许程序员团队同时开发和测试系统的多个部分。

理想情况下，存根应该 

• 检查调用者提供的环境和参数的合理性（调用带有不适当参数的函数是一个常见错误）， 

• 以符合规范的方式修改参数和全局变量，以及 

• 返回值一致 与规范。

构建足够的存根通常是一个挑战。 如果存根要替换的单元旨在执行一些复杂的任务，则构建一个执行符合规范的操作的存根可能等同于编写存根旨在替换的程序。 解决此问题的一种方法是限制存根接受的参数集，并创建一个表，其中包含要为测试套件中使用的每个参数组合返回的值。

自动化测试过程的一大吸引力在于它有助于回归测试。 当程序员试图调试程序时，安装一个“修复”来破坏以前工作的东西是很常见的。 每当进行任何更改时，无论多么小，您都应该检查程序是否仍然通过了它曾经通过的所有测试

## 6.2 Debugging

关于修复软件缺陷的过程如何被称为调试，有一个迷人的都市传说。 图 6.2 中的照片是 1947 年 9 月 9 日，在哈佛大学研究 Mark II Aiken 继电器计算器的小组的一本实验室书中的页面

![image-20210901155804981](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210901155804981.png)

一些人声称，发现困在 Mark II 中的不幸飞蛾导致使用了“调试”一词。 然而，“发现错误的第一个实际案例”的措辞表明，对该短语的不太字面的解释已经很普遍。  Mark II 项目的负责人 Grace Murray Hopper 明确表示，“bug”一词已经广泛用于描述二战期间的电子系统问题。 早在此之前，霍金斯 1896 年出版的电气手册《新电力教理》就包含这样的条目：“‘错误’一词在有限的范围内用于指明电气设备的连接或工作中的任何故障或故障。” 在英语用法中，“bugbear”一词的意思是“任何引起看似不必要或过度恐惧或焦虑的事情”。 莎士比亚似乎将其缩短为“虫子”，当时他让哈姆雷特·克维奇 (Hamlet kvetch) 谈论“我生命中的虫子和妖精”。  “bug”这个词的使用有时会导致人们忽略一个基本事实，即如果你编写了一个程序并且它有一个“bug”，你就搞砸了。 错误不会随意爬入完美无瑕的程序中。 如果你的程序有错误，那是因为你把它放在那里。 错误不会在程序中滋生。 如果您的程序有多个错误，那是因为您犯了多个错误。 运行时错误可以从两个维度进行分类：

• 显性→隐性：显性错误具有明显的表现形式，例如，程序崩溃或运行时间比应有的时间长得多（可能永远）。 隐蔽的错误没有明显的表现。 程序可以毫无问题地得出结论——除了提供不正确的答案。 许多错误介于这两个极端之间，错误是否明显取决于人们对程序行为的仔细检查。

• 持续→ 间歇性：每次使用相同输入运行程序时，都会出现持续性错误。 间歇性错误仅在某些时候发生，即使程序在相同的输入上运行并且看起来在相同的条件下也是如此。 当我们进入第 14 章时，我们将开始编写程序来模拟随机性起作用的情况。 在此类程序中，间歇性错误很常见。

最好的错误类型是公开的和持久的。 开发人员不能对部署该程序的可取性抱有幻想。 如果其他人愚蠢到试图使用它，他们很快就会发现自己的愚蠢。

也许程序在崩溃之前会做一些可怕的事情，例如，删除文件，但至少用户有理由担心（如果不是惊慌失措）。 优秀的程序员试图以这样一种方式编写他们的程序，即编程错误会导致明显且持久的错误。 这通常称为防御性编程。

进入不受欢迎坑的下一步是公开但间歇性的错误。一个几乎所有时间都计算飞机正确位置的空中交通管制系统比一个总是犯明显错误的系统要危险得多。 一个人可以在傻瓜的天堂里生活一段时间，甚至可能会部署一个包含有缺陷程序的系统，但迟早会发现错误。 如果促使错误变得明显的条件很容易重现，那么追踪和修复问题通常相对容易。 如果引发错误的条件不清楚，生活就会困难得多。

以隐蔽方式失败的程序通常非常危险。 由于它们显然没有问题，人们使用它们并相信它们会做正确的事情。 社会越来越依赖软件来执行超出人类执行甚至检查正确性能力范围的关键计算。

因此，程序可以长时间提供未被发现的错误答案。 此类程序可能并且已经造成了很多损害。评估抵押债券投资组合风险并自信地吐出错误答案的程序可能会给银行（也许是整个社会）带来很多麻烦。 放射治疗机的辐射量比预期多一点或少一点，这可能是癌症患者生死之间的区别。 一个只偶尔犯隐蔽错误的程序可能会或可能不会比总是犯这种错误的程序造成的破坏少。 隐蔽的和间歇性的错误几乎总是最难找到和修复的

### 6.2.1 Learning to Debug

调试是一项习得的技能。 没有人会本能地做好。 好消息是它不难学习，而且是一种可转移的技能。 用于调试软件的相同技能可用于找出其他复杂系统的问题，例如实验室实验或生病的人。

至少四十年来，人们一直在构建称为调试器的工具，并且所有流行的 Python IDE 中都内置了调试工具。 这些应该帮助人们在他们的程序中找到错误。 他们可以提供帮助，但只有一点点。 更重要的是你如何处理问题。 许多有经验的程序员甚至不介意调试工具。 大多数程序员说最重要的调试工具是打印语句。

当测试表明程序以不良方式运行时，调试开始。 调试是寻找该行为的解释的过程。 始终擅长调试的关键是系统地进行搜索。从研究可用数据开始。 这包括测试结果和程序文本。 研究所有的测试结果。 不仅要检查显示存在问题的测试，还要检查那些看起来运行良好的测试。

试图了解为什么一项测试有效而另一项无效的原因通常很有启发性。 在查看程序文本时，请记住您并不完全理解它。 如果你这样做了，可能不会有错误。

接下来，形成一个您认为与所有数据一致的假设。假设可以窄到“如果我将第 403 行从 x < y 更改为 x <= y，问题就会消失”，也可以宽到“我的程序没有终止，因为我在某些 while 循环中有错误的退出条件 。” 接下来，设计并运行一个有可能反驳假设的可重复实验。 例如，您可以在每个 while 循环前后放置一条打印语句。 如果这些总是成对的，那么 while 循环导致非终止的假设就被驳倒了。 在运行实验之前决定如何解释各种可能的结果。 如果你等到运行实验之后，你更有可能陷入一厢情愿的想法。

最后，记录您尝试过的实验很重要。当您花费大量时间更改代码试图追踪难以捉摸的错误时，很容易忘记您已经尝试过的内容。 如果您不小心，很容易在一遍又一遍地尝试同一个实验（或者更有可能是一个看起来不同但会给您相同信息的实验）上浪费太多时间。 请记住，正如许多人所说，“疯狂就是一遍又一遍地做同样的事情，却期待不同的结果。

### 6.2.2 Designing the Experiment

将调试视为一个搜索过程，而每个实验都是为了减少搜索空间的大小。 减小搜索空间大小的一种方法是设计一个实验，该实验可用于确定特定代码区域是否对集成测试期间发现的问题负责。 减少搜索空间的另一种方法是减少引起错误表现所需的测试数据量。让我们看一个人为的例子，看看如何调试它。 假设您编写了图 6.3 中的回文检查代码。

```python
def isPal(x):
    """Assumes x is a list
       Returns True if the list is a palindrome; False otherwise"""
    temp = x
    temp.reverse
    if temp == x:
        return True
    else:
        return False
def silly(n):
    """Assumes n is an int > 0
       Gets n inputs from user
       Prints 'Yes' if the sequence of inputs forms a palindrome;
             'No' otherwise"""
    for i in range(n):
        result = []
        elem = input('Enter element: ')
        result.append(elem)
    if isPal(result):
        print('Yes')
    else:
        print('No')
```

现在，想象一下您对自己的编程技能非常有信心，以至于您将这些代码放到了 Web 上——而没有对其进行测试。 进一步假设您收到一封电子邮件，内容是“我测试了您的 !!**！ 在以下 1000 字符串输入上运行程序，并打印 Yes。 然而，任何傻瓜都能看出它不是回文。 修理它！” 您可以尝试在提供的 1000 字符串输入上测试它。 但从较小的东西上开始尝试可能更明智。 事实上，在最小的非回文上测试它是有意义的，例如，

```python
>>> silly(2)
Enter element: a
Enter element: b
```

好消息是它即使是这个简单的测试也失败了，所以你不必输入一千个字符串。 坏消息是你不知道为什么它失败了。

在这种情况下，代码足够小，您可能可以盯着它并找到错误（或错误）。 但是，让我们假设这样做太大了，并开始系统地减少搜索空间。

通常，最好的方法是进行二分搜索。 在代码的中途找到某个点，并设计一个实验，让您可以确定在该点之前是否存在可能与症状相关的问题。  （当然，在那一点之后也可能有问题，但通常最好一次追查一个问题。）在选择这样一个点时，寻找一个有一些易于检查的中间值的地方，这些值提供有用的 信息。 如果中间值不是您所期望的，则代码中可能在该点之前发生了问题。 如果中间值看起来都很好，那么错误可能位于代码后面的某个地方。

可以重复此过程，直到您将问题所在的区域缩小到几行代码为止。傻傻地看着，如果isPal(result)，中间点就在这条线附近。 要检查的显而易见的事情是结果是否具有预期值 ['a', 'b']。 我们通过在愚蠢的 if 语句之前插入语句 print(result) 来检查这一点。 当实验运行时，程序打印 ['b']，表明出现了问题。 下一步是大约在循环中途打印结果。 这很快表明 result 的长度永远不会超过一个元素，这表明 result 的初始化需要移到 for 循环之外。

愚蠢的“更正”代码是

```python
def silly(n):
    """Assumes n is an int > 0
       Gets n inputs from user
       Prints 'Yes' if the sequence of inputs forms a palindrome;
           'No' otherwise"""
result = []
for i in range(n):
    elem = input('Enter element: ')
    result.append(elem)
print(result)
if isPal(result):
   print('Yes')
else:
   print('No')
```

让我们尝试一下，看看结果在 for 循环后是否具有正确的值。 确实如此，但不幸的是，该程序仍会打印 Yes。 现在，我们有理由相信第二个错误位于打印语句下方。 那么，让我们看看isPal。  if temp == x: 的代码行大约是该函数的一半。 所以，我们插入一行

```python
print(temp, x)
```

在那条线之前。 当我们运行代码时，我们看到 temp 具有预期值，但 x 没有。 向上移动代码，我们在代码 temp = x 之后插入一个打印语句，发现 temp 和 x 的值都为 ['a', 'b']。 快速检查代码发现，在 isPal 中我们编写了 temp.reverse 而不是 temp.reverse()——temp.reverse 的评估返回列表的内置 reverse 方法，但没有调用它。 

我们运行测试 再次，现在似乎 temp 和 x 都有值 ['b','a']。 我们现在已将错误缩小到一行。 似乎 temp.reverse() 意外地改变了 x 的值。 一个别名错误困扰着我们：temp 和 x 是同一个列表的名称，在列表反转之前和之后。

修复它的一种方法是用 temp = x[:] 替换 isPal 中的第一个赋值语句，这会导致生成 x 的副本。

isPal 的修正版本是

```python
def isPal(x):
    """Assumes x is a list
       Returns True if the list is a palindrome; False                    otherwise"""
    temp = x[:]
    temp.reverse()
    if temp == x:
       return True
    else:
       return False
```

### 6.2.3 When the Going Gets Tough

据说美国总统约翰·肯尼迪的父亲约瑟夫·P·肯尼迪教导他的孩子们：“当事情变得艰难时，艰难的开始。”但他从未调试过任何软件。 本小节包含一些实用提示，说明当调试变得困难时该怎么办。

• 寻找常见的嫌疑人。 例如，您是否 

o 以错误的顺序将参数传递给函数， 

o 拼错名称，例如，本应键入大写字母时却键入了小写字母， 

o 无法重新初始化变量， 

o 测试两个浮点值是否为 相等 (==) 而不是几乎相等（请记住，浮点算术与您在学校学到的算术不同）， 

o 测试值相等（例如，通过编写表达式 L1 == L2 比较两个列表）当您 意味着对象相等（例如，id(L1) == id(L2)），

o 忘记了某些内置函数有副作用，

o 忘记了将函数类型的对象的引用转换为函数调用的 ()  , 

o 创建了一个无意的别名，或者 

o 犯了任何其他典型的错误。

• 不要问自己为什么程序没有按照您的意愿行事。 相反，问问自己为什么它在做什么。 这应该是一个更容易回答的问题，并且可能是弄清楚如何修复程序的良好第一步。

• 请记住，该错误可能不在您认为的位置。 如果是这样，你很可能早就找到了。 决定去哪里寻找的一种实用方法是询问错误不能在哪里。 正如福尔摩斯所说，“排除所有其他因素，剩下的一定是真相。” 

• 尝试向其他人解释问题。 我们都有盲点。 通常情况下，仅仅试图向某人解释问题就会让你看到你错过的东西。 尝试解释的一件好事是为什么错误不能出现在某些地方。

• 不要相信你读到的一切。 特别是，不要相信文档。代码可能没有按照评论的建议去做。

• 停止调试并开始编写文档。 这将帮助您从不同的角度处理问题。

• 走开，明天再试。 这可能意味着错误修复的时间比您坚持使用它的时间晚，但您可能会花费更少的时间来寻找它。 也就是说，可以用延迟换取效率。

（学生们，这是尽早开始解决编程问题集的一个很好的理由！）

### 6.2.4 When You Have Found ”The“ Bug

当您认为自己在代码中发现了错误时，开始编码和测试修复程序的诱惑几乎是无法抗拒的。 然而，慢一点通常会更好。 请记住，目标不是修复一个错误，而是快速有效地实现无错误程序。

问问自己这个错误是否解释了所有观察到的症状，或者它是否只是冰山一角。 如果是后者，最好考虑与其他更改一起处理此错误。 例如，假设您发现错误是意外改变列表的结果。 您可以在本地绕过该问题，或许可以通过制作列表的副本。 或者，您可以考虑使用元组而不是列表（因为元组是不可变的），或许可以消除代码中其他地方的类似错误。

在进行任何更改之前，请尝试了解所提议的“修复”的后果。 它会破坏其他东西吗？ 它是否引入了过多的复杂性？它是否提供了整理代码其他部分的机会？

始终确保您可以回到原来的位置。 没有什么比意识到一连串的变化让你比开始时离目标更远，并且无法回到起点更令人沮丧的了。 磁盘空间通常充足。 用它来存储程序的旧版本。

最后，如果有许多无法解释的错误，您可能会考虑一次查找和修复一个错误是否是正确的方法。 也许你最好考虑一下是否有更好的方法来组织你的程序，或者一些更简单的算法更容易正确实现。

# 7 EXCEPTIONS AND ASSERTIONS

“例外”通常被定义为“不符合规范的事情”，因此有点罕见。  Python 中的异常并不罕见。 他们无处不在。 实际上，标准 Python 库中的每个模块都使用它们，并且 Python 本身会在许多不同的情况下引发它们。

你已经看过其中的一些了。打开一个 Python shell 并输入

```python
test = [1,2,3]
test[3]
```

shell 会用类似的东西回应

```python
IndexError: list index out of range
```

IndexError 是 Python 在程序尝试访问可索引类型范围之外的元素时引发的异常类型。  IndexError 后面的字符串提供了有关导致异常发生的原因的附加信息。Python 的大多数内置异常处理程序试图执行没有适当语义的语句的情况。
  （我们将在本章后面处理例外的异常——那些不处理错误的异常。）

那些试图编写和运行 Python 程序的读者（我们希望你们所有人）已经遇到过很多这样的异常。 最常见的异常类型包括 TypeError、IndexError、NameError 和 ValueError 

## 7.1 Handling Exceptions

到目前为止，我们将异常视为致命事件。 当引发异常时，程序终止（在这种情况下崩溃可能是一个更合适的词），然后我们返回到我们的代码并试图找出出了什么问题。 当引发导致程序终止的异常时，我们说引发了未处理的异常。

异常不需要导致程序终止。 异常发生时，可以而且应该由程序处理。 有时会因为程序中存在错误（例如访问不存在的变量）而引发异常，但很多时候，异常是程序员可以并且应该预料到的。 程序可能会尝试打开不存在的文件。 如果交互式程序要求用户输入，则用户可能会输入不适当的内容。

如果您知道某行代码在执行时可能会引发异常，则应该处理该异常。 在编写良好的程序中，未处理的异常应该是异常。考虑代码

```python
successFailureRatio = numSuccesses/numFailures
print('The success/failure ratio is', successFailureRatio)
print('Now here')
```

大多数情况下，这段代码可以正常工作，但如果 numFailures 恰好为零，它将失败。 尝试除以零将导致 Python 运行时系统引发 ZeroDivisionError 异常，并且永远不会到达打印语句。

最好写一些类似的东西 

```python
try:
    successFailureRatio = numSuccesses/numFailures
    print('The success/failure ratio is', successFailureRatio)
except ZeroDivisionError:
    print('No failures, so the success/failure ratio is undefined.')
    print('Now here')
```

进入 try 块后，解释器尝试计算表达式 numSuccesses/numFailures。 如果表达式求值成功，程序将表达式的值赋给变量 successFailureRatio，在 try 块的末尾执行打印语句，并继续执行 try-except 之后的打印语句。 但是，如果在表达式计算过程中引发 ZeroDivisionError 异常，则控制立即跳转到 except 块（跳过 try 块中的赋值和打印语句），执行 except 块中的打印语句，然后继续执行 try-except 块后面的打印语句。

练习：实现一个满足以下规范的函数。 使用 try-except 块。

```python
def sumDigits(s):
    """Assumes s is a string
       Returns the sum of the decimal digits in s
         For example, if s is 'a2b3c' it returns 5"""
```

让我们再看一个例子。 考虑代码

```python
val = int(input('Enter an integer: '))
print('The square of the number you entered is', val**2)
```

如果用户乐于输入一个可以转换为整数的字符串，一切都会好起来的。 但是假设用户键入 abc？ 执行这行代码会导致 Python 运行时系统引发 ValueError 异常，并且永远不会到达打印语句。

程序员应该写的东西看起来像

```python
while True:
    val = input('Enter an integer: ')
    try:
        val = int(val)
        print('The square of the number you entered is', val**2)
        break #to exit the while loop
    except ValueError:
        print(val, 'is not an integer')
```

进入循环后，程序会要求用户输入一个整数。一旦用户输入了一些东西，程序就会执行 try-except 块。如果 try 块中的前两个语句均未引发 ValueError 异常，则执行 break 语句并退出 while 循环。但是，如果执行 try 块中的代码引发 ValueError 异常，则控制立即转移到 except 块中的代码。 因此，如果用户输入一个不代表整数的字符串，程序会要求用户再试一次。 无论用户输入什么文本，都不会导致未处理的异常。

这种变化的缺点是程序文本从两行增加到八行。 如果有很多地方要求用户输入整数，这可能会有问题。 当然，这个问题可以通过引入一个函数来解决： 

```python
def readInt():
    while True:
        val = input('Enter an integer: ')
        try:
            return(int(val)) #返回前将 str 转换为 int
        except ValueError:
            print(val, 'is not an integer')
```

更好的是，这个函数可以泛化为要求任何类型的输入：

```python
def readVal(valType, requestMsg, errorMsg):
  while True:
      val = input(requestMsg + ' ')
      try:
          return(valType(val)) #convert str to valType before    returning
      except ValueError:
          print(val, errorMsg)
            
readVal(int, 'Enter an integer:', 'is not an integer')
```

函数 readVal 是多态的，即它适用于许多不同类型的参数。 这样的函数很容易用 Python 编写，因为类型是一等对象。 我们现在可以使用代码请求一个整数

```python
val = readVal(int, 'Enter an integer:', 'is not an integer')
```

异常可能看起来不友好（毕竟，如果不处理，异常会导致程序崩溃），但请考虑替代方案。 例如，当要求将字符串 'abc' 转换为 int 类型的对象时，类型转换 int 应该做什么？ 它可以返回一个与用于对字符串进行编码的位相对应的整数，但这不太可能与程序员的意图有任何关系。 或者，它可以返回特殊值 None。 如果这样做，程序员将需要插入代码来检查类型转换是否返回了 None。 忘记检查的程序员可能会在程序执行过程中遇到一些奇怪的错误。

对于异常，程序员仍然需要包含处理异常的代码。 但是，如果程序员忘记包含此类代码并引发异常，则程序将立即停止。 这是一件好事。 它提醒程序的用户已经发生了一些麻烦的事情。（而且，正如我们在第 6 章中讨论的，公开的错误比隐蔽的错误要好得多。）此外，它可以让调试程序的人清楚地指出哪里出错了。

如果一个程序代码块可能引发不止一种异常，则保留字 except 后面可以跟一个异常元组，例如，

```python
except (ValueError, TypeError):
```

在这种情况下，如果在 try 块中引发了任何列出的异常，则将进入 except 块。

或者，我们可以为每种异常编写一个单独的 except 块，它允许程序根据引发的异常选择操作。 如果程序员写

```python
except:
```

如果在 try 块中引发任何类型的异常，则将进入 except 块。 这些功能如图 7.1 所示。

## 7.2 Exceptions as a Control Flow Mechanism

不要将异常视为纯粹的错误。 它们是一种方便的控制流机制，可用于简化程序。

在许多编程语言中，处理错误的标准方法是让函数返回一个值（通常类似于 Python 的 None），表明某些地方出了问题。 每个函数调用都必须检查该值是否已返回。 在 Python 中，当函数不能产生与函数规范一致的结果时，更常见的是让函数引发异常。

Python raise 语句强制发生指定的异常。  raise 语句的形式是

```python
raise exceptionName(arguments)
```

exceptionName 通常是内置异常之一，例如 ValueError。但是，程序员可以通过创建内置类 Exception 的子类（参见第 8 章）来定义新的异常。 不同类型的异常可以有不同类型的参数，但大多数时候参数是单个字符串，用于描述引发异常的原因。

练习：实现一个满足规范的函数

```python
def findAnEven(L):
    """Assumes L is a list of integers
       Returns the first even number in L
       Raises ValueError if L does not contain an even number""" 
```

考虑图 7.1 中的函数定义。

```python
def getRatios(vect1, vect2):
    """Assumes: vect1 and vect2 are equal length lists of numbers
       Returns: a list containing the meaningful values of
           vect1[i]/vect2[i]"""
    ratios = []
    for index in range(len(vect1)):
        try:
            ratios.append(vect1[index]/vect2[index])
        except ZeroDivisionError:
            ratios.append(float('nan')) #nan = Not a Number
        except:
            raise ValueError('getRatios called with bad arguments')
        return ratios
```

有两个与 try 块关联的 except 块。 如果在 try 块中引发异常，Python 首先检查它是否是 ZeroDivisionError。

如果是这样，它会附加一个特殊的值，nan，类型为 float 到 ratios。  （值 nan 代表“不是数字”。它没有文字，但可以通过将字符串 'nan' 或字符串 'NaN' 转换为类型 float 来表示。当 nan 在 float 类型的表达式，该表达式的值也是 nan。）如果异常不是 ZeroDivisionError，则代码执行第二个 except 块，这将引发一个带有关联字符串的 ValueError 异常。

原则上，不应进入第二个 except 块，因为调用 getRatios 的代码应遵守 getRatios 规范中的假设。 然而，由于检查这些假设只会带来微不足道的计算负担，因此无论如何练习防御性编程和检查可能是值得的。

以下代码说明了程序可能如何使用 getRatios。 除了 ValueError as msg: 之外，行中的名称 msg 绑定到与引发 ValueError 关联的参数（在本例中为字符串）。 当代码

```python
try:
    print(getRatios([1.0,2.0,7.0,6.0], [1.0,2.0,0.0,3.0]))
    print(getRatios([], []))
    print(getRatios([1.0, 2.0], [3.0]))
except ValueError as msg:
    print(msg)
```

执行它打印

```python
[1.0, 1.0, nan, 2.0]
[]
getRatios called with bad arguments
```

为了比较，图 7.2 包含相同规范的实现，但没有使用 try-except。

```python
def getRatios(vect1, vect2):
    """Assumes: vect1 and vect2 are lists of equal length of numbers
       Returns: a list containing the meaningful values of
               vect1[i]/vect2[i]"""
    ratios = []
    if len(vect1) != len(vect2):
        raise ValueError('getRatios called with bad arguments')
    for index in range(len(vect1)):
        vect1Elem = vect1[index]
        vect2Elem = vect2[index]
        if (type(vect1Elem) not in (int, float))\
          or (type(vect2Elem) not in (int, float)):
            raise ValueError('getRatios called with bad arguments')
        if vect2Elem == 0.0:
            ratios.append(float('NaN')) #NaN = Not a Number
        else:
            ratios.append(vect1Elem/vect2Elem)
     return ratios
```

图 7.2 中的代码比图 7.1 中的代码更长且更难阅读。 它的效率也较低。  （图 7.2 中的代码可以通过消除局部变量 vect1Elem 和 vect2Elem 稍微缩短，但代价是通过重复索引列表而导致效率低下。）让我们再看一个例子，图 7.3。 函数 getGrades 要么返回一个值，要么引发一个与它相关联的值的异常。 如果对 open 的调用引发 IOError，则会引发 ValueError 异常。 它可以忽略 IOError 并让调用 getGrades 的程序部分处理它，但这会向调用代码提供较少的关于出错的信息。 使用 getGrades 的代码要么使用返回值计算另一个值，要么处理异常并打印信息性错误消息。

```python
def getGrades(fname):
try:
gradesFile = open(fname, 'r') #open file for reading
except IOError:
raise ValueError('getGrades could not open ' + fname)
grades = []
for line in gradesFile:
try:
grades.append(float(line))
except:
raise ValueError('Unable to convert line to float')
return grades
try:
grades = getGrades('quiz1grades.txt')
grades.sort()
median = grades[len(grades)//2]
print('Median grade is', median)
except ValueError as errorMsg:
print('Whoops.', errorMsg)
```

## 7.3 Assertions

Python assert 语句为程序员提供了一种简单的方法来确认计算状态是否符合预期。  assert 语句可以采用以下两种形式之一：

```python
assert Boolean expression
```

或者

```python
assert Boolean expression, argument
```

当遇到 assret 语句时，将计算布尔表达式。如果它的计算结果为 True，则执行会以愉快的方式继续。 如果计算结果为 False，则会引发 AssertionError 异常。

assert 是一种有用的防御性编程工具。 它们可用于确认函数的参数是适当的类型。 它们也是一个有用的调试工具。 例如，可用于确认中间值具有预期值或函数返回可接受的值

# 8 CLASSES AND OBJECT-ORIENTED PROGRAMMING

现在，我们将注意力转向与 Python 编程相关的最后一个主要主题：使用类围绕模块和数据抽象组织程序。

类可以以多种不同的方式使用。 在本书中，我们强调在面向对象编程的上下文中使用它们。 面向对象编程的关键是将对象视为数据和操作该数据的方法的集合。

面向对象编程的思想已有四十多年的历史，在过去二十五年左右的时间里被广泛接受和实践。 在 1970 年代中期，人们开始撰写文章解释这种编程方法的好处。 大约在同一时间，编程语言 SmallTalk（在 Xerox PARC）和 CLU（在 MIT）为这些想法提供了语言支持。 但直到 C++ 和 Java 的到来，它才真正在实践中起飞。

在本书的大部分时间里，我们一直隐含地依赖于面向对象的编程。 回到 2.1.1 节，我们说过“对象是 Python 程序操作的核心内容。 每个对象都有一个类型，它定义了程序可以对那个对象做的事情的种类。” 从第 2 章开始，我们依赖于内置类型，例如 list 和 dict 以及与这些类型相关的方法。 但正如编程语言的设计者只能构建一小部分有用的函数一样，他们也只能构建一小部分有用的类型。 我们已经研究了一种允许程序员定义新函数的机制； 我们现在来看一种允许程序员定义新类型的机制。

## 8.1 Abstract Data Types and Classes

抽象数据类型的概念非常简单。 抽象数据类型是一组对象和对这些对象的操作。 它们绑定在一起，以便可以将对象从程序的一个部分传递到另一个部分，这样做不仅可以访问对象的数据属性，还可以访问易于操作该数据的操作。

这些操作的规范定义了抽象数据类型和程序其余部分之间的接口。 接口定义了操作的行为——它们做什么，而不是它们如何做。 因此，该接口提供了一个抽象屏障，将程序的其余部分与提供类型抽象实现所涉及的数据结构、算法和代码隔离开来。

编程是关于以促进变化的方式管理复杂性。有两种强大的机制可以实现这一点：分解和抽象。 分解在程序中创建结构，抽象抑制细节。 关键是压制适当的细节。 这就是数据抽象达到目的的地方。 可以创建提供方便抽象的特定于域的类型。 理想情况下，这些类型捕获与程序生命周期相关的概念。 如果通过设计几个月甚至几十年后相关的类型来开始编程过程，那么在维护该软件方面就有很大的优势。

在本书中，我们一直在使用抽象数据类型（没有这样称呼它们）。 我们已经使用整数、列表、浮点数、字符串和字典编写了程序，而没有考虑如何实现这些类型。
套用莫里哀的 Bourgeois Gentilhomme，“Par ma foi, il y a plus decent pages que nous avons utilisé ADTs, sans que nous le sachions。”

在 Python 中，人们使用类来实现数据抽象。 图 8.1 包含一个类定义，它提供了一个名为 IntSet 的 setofintegers 抽象的直接实现。

一个类定义创建一个类型类型的对象，并将一组类型为 instancemethod 的对象与该类对象相关联。 例如，表达式 IntSet.insert 指的是在类 IntSet 的定义中定义的方法 insert。 和代码

```python
print(type(IntSet), type(IntSet.insert))
```

将会输出

```python
<class 'type'> <class 'function'>
```

请注意，类定义顶部的 docstring（用 """ 括起来的注释）描述了类提供的抽象，而不是关于类如何实现的信息。相反，docstring 下面的注释包含有关实现的信息 . 该信息面向可能想要修改实现或构建类的子类（参见第 8.2 节）的程序员，而不是可能想要使用抽象的程序员请注意，类定义顶部的 docstring（用 """ 括起来的注释）描述了类提供的抽象，而不是关于类如何实现的信息。相反，docstring 下面的注释包含有关实现的信息 . 该信息面向可能想要修改实现或构建类的子类（参见第 8.2 节）的程序员，而不是可能想要使用抽象的程序员

```python
class IntSet(object):
"""An intSet is a set of integers"""
#Information about the implementation (not the abstraction)
#Value of the set is represented by a list of ints, self.vals.
#Each int in the set occurs in self.vals exactly once.
def __init__(self):
"""Create an empty set of integers"""
self.vals = []
def insert(self, e):
"""Assumes e is an integer and inserts e into self"""
if e not in self.vals:
self.vals.append(e)
def member(self, e):
"""Assumes e is an integer
Returns True if e is in self, and False otherwise"""
return e in self.vals
def remove(self, e):
"""Assumes e is an integer and removes e from self
Raises ValueError if e is not in self"""
try:
self.vals.remove(e)
except:
raise ValueError(str(e) + ' not found')
def getMembers(self):
"""Returns a list containing the elements of self.
Nothing can be assumed about the order of the elements"""
return self.vals[:]
def __str__(self):
"""Returns a string representation of self"""
self.vals.sort()
result = ''
for e in self.vals:
result = result + str(e) + ','
return '{' + result[:-1] + '}' #-1 omits trailing comma
```

当函数定义出现在类定义中时，定义的函数称为方法并与类相关联。 这些方法有时被称为类的方法属性。 如果目前这看起来令人困惑，请不要担心。 在本章的后面，我们将有更多关于这个主题的内容要说。

类支持两种操作： 

• 实例化用于创建类的实例。 例如，语句 s = IntSet() 创建一个 IntSet 类型的新对象。 这个对象被称为 IntSet 的一个实例。

• 属性引用使用点表示法来访问与类关联的属性。 例如，s.member 指的是与 IntSet 类型的实例 s 关联的方法成员。

每个类定义都以保留字 class 开头，后跟类的名称以及有关它与其他类的关系的一些信息。 在这种情况下，第一行表示 IntSet 是 object 的子类。 现在，忽略作为子类的含义。 我们很快就会谈到这一点。

正如我们将看到的，Python 有许多特殊的方法名称，它们以两个下划线开头和结尾。 我们将看到的第一个是 __init__。 每当实例化一个类时，都会调用该类中定义的 __init__ 方法。 当代码行

```python
s = IntSet()
```

执行时，解释器会创建一个新的 IntSet 类型实例，然后以新创建的对象作为实参调用 IntSet.__init__ 绑定到形参 self 上。 调用时，IntSet.__init__ 创建 vals，一个 list 类型的对象，它成为新创建的 IntSet 类型实例的一部分。  （列表是使用现在熟悉的符号 [] 创建的，它只是 list() 的缩写。）这个列表称为 IntSet 实例的数据属性。 请注意，每个 IntSet 类型的对象都有一个不同的 vals 列表，正如人们所期望的那样。

正如我们所见，与类的实例关联的方法可以使用点表示法调用。 例如，代码，

```python
s = IntSet()
s.insert(3)
print(s.member(3))
```

创建一个新的 IntSet 实例，将整数 3 插入该 IntSet，然后打印 True。

乍一看，这里似乎有些不一致。 看起来好像每个方法都用一个太少的参数调用。 例如，member 有两个形参，但我们似乎只用一个实参来调用它。这是点符号的产物。 与点前面的表达式关联的对象作为第一个参数隐式传递给方法。 在整本书中，我们遵循使用 self 作为绑定这个实参的形参名称的约定。  Python 程序员几乎普遍遵守这个约定，我们强烈建议您也使用它。

类不应与该类的实例混淆，就像列表类型的对象不应与列表类型混淆一样。 属性可以与类本身或与类的实例相关联： 

• 方法属性在类定义中定义，例如 IntSet.member 是类 IntSet 的属性。 当类被实例化时，例如通过语句 s = IntSet()，创建实例属性，例如 s.member。 请记住， IntSet.member 和 s.member 是不同的对象。 虽然 s.member 最初绑定到类 IntSet 中定义的成员方法，但可以在计算过程中更改该绑定。 例如，您可以（但不应该！）编写 s.member = IntSet.insert。

• 当数据属性与类相关联时，我们称它们为类变量。当它们与实例相关联时，我们称它们为实例变量。 例如，vals 是一个实例变量，因为对于类 IntSet 的每个实例，vals 绑定到不同的列表。 到目前为止，我们还没有看到类变量。 我们将使用图 8.3 中的一个。

数据抽象实现了表示独立性。 可以将抽象类型的实现视为具有多个组件： • 类型方法的实现， 

• 一起编码类型值的数据结构，以及 

• 关于方法的实现如何使用数据结构的约定。 表示不变量捕获了一个关键约定。

表示不变量定义数据属性的哪些值对应于类实例的有效表示。  IntSet 的表示不变量是 vals 不包含重复项。  __init__ 的实现负责建立不变量（持有空列表），其他方法负责维护该不变量。 这就是为什么 insert 仅在 e 不在 self.vals 中时才附加它的原因。remove 的实现利用了输入 remove 时满足表示不变量的假设。 它只调用 list.remove 一次，因为表示不变式保证在 self.vals 中最多出现一次 e。

类中定义的最后一个方法 __str__ 是另一种特殊的 __ 方法。 使用打印命令时，会自动调用与要打印的对象关联的 __str__ 函数。 例如，代码

```python
s = IntSet()
s.insert(3)
s.insert(4)
print(s)
```

将会输出

```python
{3，4}
```

（如果没有定义 __str__ 方法，执行 print(s) 会导致类似 <__main__.IntSet object at 0x1663510> 的东西被打印出来。）我们也可以通过写 print s.__str__() 甚至 print IntSet 来打印 s 的值 .__str__(s)，但使用这些形式不太方便。 当程序通过调用 str 将该类的实例转换为字符串时，也会调用该类的 __str__ 方法。

用户定义类的所有实例都是可散列的，因此可以用作字典键。 如果没有提供 __hash__ 方法，则对象的哈希值是从函数 id 派生的（参见第 5.3 节）。 如果没有提供 __eq__ 方法，则所有对象都被认为是不相等的（除了它们自己）。 如果提供了用户定义的 __hash__，则应确保对象的哈希值在该对象的整个生命周期中保持不变。

### 8.1.1 Designing Programs Using Abstract Data Types

抽象数据类型很重要。 它们导致了对组织大型程序的不同思考方式。 当我们思考世界时，我们依赖于抽象。在金融界，人们谈论股票和债券。 在生物学领域，人们谈论蛋白质和残留物。 当试图理解诸如此类的概念时，我们会在精神上将这些对象的一些相关数据和特征收集到一个智力包中。 例如，我们认为债券具有利率和到期日作为数据属性。我们还认为债券具有“设定价格”和“计算到期收益率”等操作。 抽象数据类型允许我们将这种组织方式融入到程序设计中。

数据抽象鼓励程序设计者关注数据对象的中心性而不是功能。 将程序更多地视为类型的集合而不是函数的集合会导致完全不同的组织原则。 除此之外，它鼓励人们将编程视为组合相对较大的块的过程，因为数据抽象通常比单个函数包含更多的功能。这反过来又使我们将编程的本质视为一个过程，而不是编写单独的代码行，而是组合抽象。

可重用抽象的可用性不仅减少了开发时间，而且通常会导致更可靠的程序，因为成熟的软件通常比新软件更可靠。 多年来，唯一常用的程序库是统计或科学的。 然而，今天有大量可用的程序库（尤其是 Python），通常基于一组丰富的数据抽象，我们将在本书后面看到。

### 8.1.2 Using Classes to Keep Track of Students and Faculty

作为类的使用示例，假设您正在设计一个程序来帮助跟踪一所大学的所有学生和教职员工。 当然可以在不使用数据抽象的情况下编写这样的程序。 每个学生都有姓氏、名字、家庭住址、年份、成绩等。这些都可以保存在列表和字典的某种组合中。 跟踪教职员工将需要一些类似的数据结构和一些不同的数据结构，例如，数据结构来跟踪诸如工资历史之类的事情。

在急于设计一堆数据结构之前，让我们考虑一些可能证明有用的抽象。 是否存在涵盖学生、教授和教职员工共同属性的抽象？ 有些人会争辩说他们都是人。 图 8.2 包含一个类，该类包含人类的一些常见属性（姓名和生日）。 它利用了标准 Python 库模块 datetime，它提供了许多创建和操作日期的便捷方法。

```python
import datetime
class Person(object):
def __init__(self, name):
"""Create a person"""
self.name = name
try:
lastBlank = name.rindex(' ')
self.lastName = name[lastBlank+1:]
except:
self.lastName = name
self.birthday = None
def getName(self):
"""Returns self's full name"""
return self.name
def getLastName(self):
"""Returns self's last name"""
return self.lastName
def setBirthday(self, birthdate):
"""Assumes birthdate is of type datetime.date
Sets self's birthday to birthdate"""
self.birthday = birthdate
def getAge(self):
"""Returns self's current age in days"""
if self.birthday == None:
raise ValueError
return (datetime.date.today() - self.birthday).days
def __lt__(self, other):
"""Returns True if self precedes other in alphabetical
order, and False otherwise. Comparison is based on last
names, but if these are the same full names are
compared."""
if self.lastName == other.lastName:
return self.name < other.name
return self.lastName < other.lastName
def __str__(self):
"""Returns self's name"""
return self.name
```

以下代码使用了 Person。

```python
me = Person('Michael Guttag')
him = Person('Barack Hussein Obama')
her = Person('Madonna')
print(him.getLastName())
him.setBirthday(datetime.date(1961, 8, 4))
her.setBirthday(datetime.date(1958, 8, 16))
print(him.getName(), 'is', him.getAge(), 'days old')
```

请注意，每当 Person 被实例化时，都会向 __init__ 函数提供一个参数。 通常，在实例化一个类时，我们需要查看该类的 __init__ 函数的规范，以了解要提供哪些参数以及这些参数应该具有哪些属性。上述代码执行后，会出现Person类的三个实例。

然后可以使用与它们关联的方法访问有关这些实例的信息。 例如，him.getLastName() 将返回'奥巴马'。 表达式 he.lastName 也将返回 'Obama'； 然而，出于本章稍后讨论的原因，编写直接访问实例变量的表达式被认为是糟糕的形式，应该避免。 类似地，Person 抽象的用户没有合适的方法来提取一个人的生日，尽管该实现包含具有该值的属性。  （当然，向类中添加 getBirthday 方法会很容易。）但是，有一种方法可以根据人的生日提取信息，如上述代码中的最后一个打印语句所示。

类 Person 定义了另一个特别命名的方法，__lt__。 此方法重载 < 运算符。 只要 < 运算符的第一个参数是 Person 类型，就会调用 Person__lt__ 方法。  Person 类中的 __lt__ 方法是使用 str 类型的二元 < 运算符实现的。 表达式 self.name < other.name 是 self.name.__lt__(other.name) 的简写。 由于 self.name 是 str 类型，所以这个 __lt__ 方法是与 str 类型关联的方法。

除了提供编写使用 < 的中缀表达式的语法便利之外，此重载还提供对使用 __lt__ 定义的任何多态方法的自动访问。 内置方法 sort 就是这样一种方法。 因此，例如，如果 pList 是由 Person 类型的元素组成的列表，则调用 pList.sort() 将使用类 Person 中定义的 __lt__ 方法对该列表进行排序。

代码

```python
pList = [me, him, her]
for p in pList:
    print(p)
pList.sort()
for p in pList:
    print(p)
```

第一次会输出

```python
Michael Guttag
Barack Hussein Obama
Madonna
```

之后输出

```python
Michael Guttag
Madonna
Barack Hussein Obama
```

## 8.2 Inheritance

许多类型具有与其他类型相同的属性。 例如，类型 list 和 str 每个都有 len 函数，意思相同。 继承为构建相关抽象组提供了一种方便的机制。 它允许程序员创建一个类型层次结构，其中每个类型都从层次结构中它上面的类型继承属性。

类对象位于层次结构的顶部。 这是有道理的，因为在 Python 中，运行时存在的一切都是对象。 因为 Person 继承了对象的所有属性，所以程序可以将变量绑定到 Person，将 Person 附加到列表等。

图 8.3 中的 MITPerson 类从其父类 Person 继承属性，包括 Person 从其父类 object 继承的所有属性。用面向对象编程的术语来说，MITPerson 是 Person 的子类，因此继承了其超类的属性。 除了继承的内容，子类还可以























































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































































