# PythonTeaching

By Soren(aka Musheng-bot in github)

## 01 Variables

### 什么是变量

变量是一个可以储存值的量，可以实现运算，特定的值的复用等等操作。

变量是我们编程的基础，在python中，任何一个变量都需要有以下两个要素: 

- 类型
- 值

### 声明并定义一个变量

在声明时，我们必须给变量赋予初值，不能像下面这样定义变量

```python
a # Invalid
b # Invalid
```

应该像这样定义

```python
a = 114514  # Valid
b = 1919810 # Valid
```

### 变量标识符规则

什么是变量标识符？就是你的`a`,`b`这样的符号，当然你可以把这个标识符写得复杂一点，像这样

```python
hello_it_is_the_python_teaching_document_written_by_Soren = 0b0100100001100101011011000110110001101111001000000101011101101111011100100110110001100100 # Valid
```

> 好奇这串二进制数字是什么的朋友可以把它翻译成字符串看看

不过我们写标识符的时候还是要遵循以下规则：

1. 只能由小写字母，大写字母，数字，下划线组成
2. 不能由数字开头

```python
# Valid identifiers
abc = 2
_car = 3
worker1 = 4
diligent_2 = 5
_ = 6

# Invalid identifiers
1_car = 7
34wer = 8
```

### 基础类型

python中有四种常用的基础类型，分别是`整型`，`浮点型`，`字符串`，`布尔型`。

```python
# Integer
a = 1
b = 2

# Float
c = 1.5
d = 2.0
scientific_number = 1e2 # 这是科学技术法标识的，e代表10^，这个数是100.0
# 科学技术法表示的数都是浮点型

# String
e = "Hello World!"
f = "jessie"
Lancer = 'dead' # 单双引号都是表示字符串

# Boolean
is_true = True # 布尔型表示真和假，用于逻辑判断
caught = False

# 特殊进制的整数
binary_number = 0b1011 # 二进制数
oct_number = 0o234 # 八进制数
hex_number = 0xFFFFFFFF # 十六进制数
```

### 字面量

字面量的概念很简单，就是像字面意思一样的量，比如`1`,`2.3`,`"Hi"`，你一看就知道他们是什么。

字面量自带两个概念，一个是`值`，一个是`类型`(毕竟你一眼就能看出来)，比如`1`是值为`1`的`整型`数。  
所以字面量可以看作是一种变量，只不过是字面量是不可修改的(你大概也想不到怎么修改一个字面量，这看起来就很诡异)。

### 常量

一种特殊的变量，不可修改的变量。

在python中的常量一般只有字面量，也没有一个正统的方便的方式像其他语言那样定义常量，所以我们一般是靠程序员自己约束。  
一般我们把常量命名成`大写字母+下划线`的形式来表示它是常量。
```python
IM_CONST = 32
YES = 1
NO = "NO"
WE_OFTEN_DO_NOT_USE_NUMBERS = "Sure"
```

### 字符串和编码

### 查看类型信息

### 类型之间的转换

### 课后练习

