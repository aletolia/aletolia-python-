# aletolia-python
introduction to computation and programing using python
### CHAPTER 1 GETTING START
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

