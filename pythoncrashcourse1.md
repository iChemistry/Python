# Python编程：从入门到实践
-----
## 第一部分 基础知识
### 第1章&emsp;起步（P11）

##### 1.&emsp;安装文本编译器：  
（1）[Sumlime Text](http://www.sublimetext.com/);  
（2）[Notepad++](https://notepad-plus-plus.org/)  

##### 2.&emsp;在 Windows 系统中从终端运行 Python 程序：  
>在命令窗口中，要在文件系统中导航，可使用终端命令 **`cd`** ；要列出当前目录中的所有文件，可使用命令 **`dir`** （表示目录，directory ）。  

### 第2章&emsp;变量和简单数据类型（P17） 
 
##### 1.&emsp;运行 hello_world.py 时发生的情况：  
>编写程序时，编辑器会以各种方式突出程序的不同部分。例如，它知道 **`print`** 是一个函数的名称，因此将其显示为蓝色；它知道 **`“Hello Python world!”`** 不是 Python 代码，因此将其显示为橙色。这种功能称为 语法突出 ，在你刚开始编写程序时很有帮助。  
  
##### 2.&emsp;变量：    

>**在本章中，你将学习可在 Python 程序中使用的各种数据，还将学习如何将数据存储到变量中，以及如何在程序中使用这些变量。**  

下面来尝试在 **`hello_world.py`** 中使用一个变量。在这个文件开头添加一行代码，并对第 2 行代码进行修改，如下所示：  

	message = "Hello Python world!"  
	print(message)  

运行这个程序，看看结果如何。你会发现，输出与以前相同：  

	Hello Python world!  

我们添加了一个名为 **`message`** 的变量 。**每个变量都存储了一个 值 —— 与变量相关联的信息**。在这里，存储的值为文本 **`“Hello Python world!”`** 。  

下面来进一步扩展这个程序：修改 **`hello_world.py`** ，使其再打印一条消息。为此，在 **`hello_world.py`** 中添加一个空行，再添加下面两行代码：  

	message = "Hello Python world!"  
	print(message)  
  
	message = "Hello Python Crash Course world!"  
	print(message)    

现在如果运行这个程序，将看到两行输出：  

	Hello Python world!  
	Hello Python Crash Course world!  

>**在程序中可随时修改变量的值，而 Python 将始终记录变量的最新值。**  

##### 3.&emsp;字符串:  
>**字符串 就是一系列字符。在 Python 中，用引号括起的都是字符串，其中的引号可以是单引号，也可以是双引号。**   

（1）使用**方法**修改字符串的大小写：  
对于字符串，可执行的最简单的操作之一是**修改其中的单词的大小写**。请看下面的代码，并尝试判断其作用：  
   
**name.py**   
  
	name = "ada lovelace"
	print(name.title())  

将这个文件保存为 **`name.py`** ，再运行它。你将看到如下输出：  
  
	Ada Lovelace  
   
>在这个示例中，小写的字符串 **`"ada lovelace"`** 存储到了变量 **`name`** 中。在 **`print()`** 语句中，方法 **`title()`** 出现在这个变量的后面。 方法 是 Python 可对数据执行的操作。
在 **`name.title()`** 中， **`name`** 后面的句点（ . ）让 Python 对变量 **`name`** 执行方法 **`title()`** 指定的操作。每个方法后面都跟着一对括号，这是因为方法通常需要额外的信息来完成
其工作。这种信息是在括号内提供的。函数 **`title()`** 不需要额外的信息，因此它后面的括号是空的。  

	name = "Ada Lovelace"  
	print(name.upper()) 全变大写   
	print(name.lower()) 全变小写    
  
（2）合并（拼接）字符串：  
在很多情况下，都需要合并字符串。例如，你可能想将姓和名存储在不同的变量中，等要显示姓名时再将它们合而为一：  

	first_name = "ada"  
	last_name = "lovelace"  
	full_name = first_name+""+last_name  
  
	print("Hello, "+full_name.title()+"!")  
	Hello, Ada Lovelace!    

（在这里，一个问候用户的句子中使用了全名，并使用了方法 **`title()`** 来将姓名设置为合适的格式。）  
  
你可以使用拼接来创建消息，再把整条消息都存储在一个变量中：  
  
	first_name = "ada"  
	last_name = "lovelace"  
	full_name = first_name+""+last_name  

	message = "Hello, "+full_name.title()+"!"  
	print(message)   
	Hello, Ada Lovelace!  

上述代码也显示消息 **`“Hello, Ada Lovelace!”`** ，但将这条消息存储在了一个变量中，这让最后的 **`print`** 语句简单得多。  
  
（3）使用制表符或换行符来添加空白：  
在编程中，**空白** 泛指任何非打印字符，如空格、制表符和换行符。你可使用空白来组织输出，以使其更易读。  
要在字符串中添加**制表符**，可使用字符组合 **`\t`** ，如：   
 
	>>>print("python")  
	python   
	>>>print("\tpython")   
	    python   

要在字符串中添加**换行符**，可使用字符组合 **`\n`** ：   
   
	>>>print("Languages:\nPython\nC\nJavaScript")   
	Languages:  
	Python  
	C  
	Java  
  
还可在同一个字符串中同时包含制表符和换行符。字符串 **`"\n\t"`** 让 Python 换到下一行，并在下一行开头添加一个制表符。下面的示例演示了如何使用一个单行字符串来生成四行
输出：  
   
	>>>print("Languages:\n\tPython\n\tC\n\tJavaScript")  
	    Languages:  
	    Python  
	    C  
	    JavaScript   
   
在接下来的两章中，你将使用为数不多的几行代码来生成很多行输出，届时**制表符**和**换行符**将提供极大的帮助。  

（4）删除空白：   
在程序中，额外的空白可能令人迷惑。对程序员来说， **`'python'`** 和 **`'python '`** 看起来几乎没什么两样，但对程序来说，它们却是两个不同的字符串。  
所幸在 Python 中，删除用户输入的数据中的多余的空白易如反掌。   
Python 能够找出字符串开头和末尾多余的空白。要确保字符串末尾没有空白，可使用**方法** **`rstrip()`** 。  
  
	>>>favorite_language = 'python '  
	>>>favorite_language  
	'python '   
	>>>favorite_language.rstrip()  
	'python'   
	>>>favorite_language   
	'python '     

存储在变量 **`favorite_language`** 中的字符串末尾包含多余的空白。你在终端会话中向 Python 询问这个变量的值时，可看到末尾的空格。对变量 **`favorite_language`** 调用方法 **`rstrip()`** 后，这个多余的空格被删除了。然而，这种删除只是暂时的，接下来再次询问 **`favorite_language`** 的值时，你会发现这个字符串与输入时一样，依然包含多余的空白。     
  
要永久删除这个字符串中的空白，必须将删除操作的结果**存回到变量**中：    
  
	>>>favorite_language = 'python '  
	>>>favorite_language = favorite_language.rstrip()     
	>>>favorite.language   
	'python'   
   
为删除这个字符串中的空白，你需要将其末尾的空白剔除，再将结果存回到原来的变量中。在编程中，经常需要修改变量的值，再将新值存回到原来的变量中。**这就是变量的值可能随程序的运行或用户输入数据而发生变化的原因**。   
  
你还可以剔除字符串开头的空白，或同时剔除字符串两端的空白。为此，可分别使用方法 **`lstrip()`** 和 **`strip()`**。  
  
##### 4.&emsp;数字：  
  
在编程中，经常使用数字来记录游戏得分、表示可视化数据、存储 Web 应用信息等。 Python 根据数字的用法以不同的方式处理它们。鉴于整数使用起来最简单，下面就先来看看Python 是如何管理它们的。  
   
（1）整数：  
在 Python 中，可对整数执行加（ + ）减（ - ）乘（ * ）除（ / ）运算。  
  
在终端会话中， Python 直接返回运算结果。 Python 使用**两个乘号**表示乘方运算：   
  
	>>>3**2  
	9  
	>>>3**3  
	27  
	>>>10**6   
	1000000   
  
（2）浮点数：  
Python 将带小数点的数字都称为**浮点数** 。   
 
（3）使用函数 str()  避免类型错误：  
你经常需要在消息中使用变量的值。例如，假设你要祝人生日快乐，可能会编写类似于下面的代码：  
  
**birthday.py**    
  
    age = 23  
    message = "Happy "+ age + "rd Birthday"  
      
    print(message)    
  
你可能认为，上述代码会打印一条简单的生日祝福语： **Happy 23rd birthday!** 。但如果你运行这些代码，将发现它们会引发错误：  
   
    Traceback(most recent call last):  
      File "birthday.py",line 2, in <module>  
       message = "Happy "+age+"rd Birthday!"  
    TypeError:Can't convert 'int' object to str implicitly  
    
这是一个 **类型错误** ，意味着 Python 无法识别你使用的信息。在这个示例中， Python 发现你使用了一个值为**整数（ int ）的变量**，但它不知道该如何解读这个值。 Python 知道，这个变量表示的可能是数值23 ，也可能是字符 2 和 3 。像上面这样在字符串中使用整数时，需要显式地指出你希望 Python 将这个整数用作字符串。为此，可调用函数 ** `str()` ** ，它让 Python 将非字符串值表示为字符串：    
  
    age = 23
    message = "Happy " + str(age) + "rd Birthday!"  
    
    print(message)   
    Happy 23rd Birthday！    
  
大多数情况下，在 Python 中使用数字都非常简单。如果结果出乎意料，请检查 Python 是否按你期望的方式将数字解读为了数值或字符串。  
  
##### 5.&emsp;注释：  
  
在 Python 中，注释用井号** ( # ) **标识。   
  
>如果程序太简单，实在没有什么需要说明的，就在程序文件开头加上你的姓名和当前日期，再用一句话阐述程序的功能。   
  
##### 6.&emsp;Pyhthon 之禅（the Zen of Python）：  
  
Python 之禅： 在 Python 终端会话中执行命令 **`import this`**。  
  

  

  
  



      




  
  
