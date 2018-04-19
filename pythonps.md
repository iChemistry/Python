## python的一些小细节:
1.在程序中可随时修改变量的值，而 Python 将始终记录变量的**最新值**。

2.**字符串**就是一系列字符。在 Python 中，用引号括起的都是字符串，其中的引号可以是单引号，也可以是双引号。  
  
3.**name.py**   

	name = 'ada lovelace'  
	print(name.tittle())     
运行后:   

	Ada Lovelace
   
在这个示例中，小写的字符串 `"ada lovelace"` 存储到了变量 name 中。在 print() 语句中，**方法title()**出现在这个变量的后面。方法 是 Python 可对**数据**执行的操作。
  
在 name.title() 中， name 后面的句点（ . ）让 Python 对变量 name 执行方法 title() 指定的操作。每个方法后面都跟着一对括号，这是因为方法通常需要额外的信息来完成其工作。**这种信息是在括号内提供的**。**函数 title() 不需要额外的信息，因此它后面的括号是空的**。
  
4.**使用制表符或换行符来添加空白**  

在编程中，**空白** 泛指任何非打印字符，如空格、制表符和换行符。你可使用空白来组织输出，以使其更易读。  
要在字符串中添加制表符，可使用字符组合 **`\t`** ，如下所示：    
  
	>>>print('Python')` 
	Python 
	>>>print('\tPython')  
	    Python   
 
要在字符串中添加换行符，可使用字符组合 **`\n`** ：  

	>>>print('Language:\nPython\nC\nJava')  
	Language:  
	Python  
	C  
	Java  

还可在同一个字符串中同时包含制表符和换行符。字符串 **`"\n\t"`** 让 Python 换到下一行，并在下一行开头添加一个制表符。    

	>>>print('Langauage:\n\tPython\n\tC\n\tJava')    
	    Language:    
	    Python    
	    C     
	    Java     

5.Python 使用**两个乘号表示乘方运算**。 
 
6.**注释**让你能够使用自然语言在程序中添加说明。
  
如果程序太简单，实在没有什么需要说明的，就在程序文件开头加上你的姓名和当前日期，再用一句话阐述程序的功能  