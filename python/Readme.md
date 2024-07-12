第三期-书生大模型实战训练营学习记录python入门

### 任务一



请实现一个wordcount函数，统计英文字符串中每个单词出现的次数。返回一个字典，key为单词，value为对应单词出现的次数。

Eg:

Input:

"""Hello world!  
This is an example.  
Word count is fun.  
Is it fun to count words?  
Yes, it is fun!"""

Output:

{'hello': 1,'world!': 1,'this': 1,'is': 3,'an': 1,'example': 1,'word': 1, 
'count': 2,'fun': 1,'Is': 1,'it': 2,'to': 1,'words': 1,'Yes': 1,'fun': 1  }

TIPS：记得先去掉标点符号,然后把每个单词转换成小写。不需要考虑特别多的标点符号，只需要考虑实例输入中存在的就可以。

text = """
Got this panda plush toy for my daughter's birthday,
who loves it and takes it everywhere. It's soft and
super cute, and its face has a friendly look. It's
a bit small for what I paid though. I think there
might be other options that are bigger for the
same price. It arrived a day earlier than expected,
so I got to play with it myself before I gave it
to her.
"""

def wordcount(text):
    pass

### 任务二



使用本地vscode连接远程开发机，写的wordcount函数在开发机上进行debug，体验debug的全流程，并完成一份debug笔记(需要截图)。



### 一、编写测试代码

我们可以使用Python的内置调

将我们的`wordcount`函数和测试代码保存到一个名为`word_count.py`的文件中：

# word_count.py


![1720771482173_9A00890B-2B8C-4055-9333-2C9278314A6F](/images/1720771482173_9A00890B-2B8C-4055-9333-2C9278314A6F.png)

1.使用replace方法去掉标点符号

2.使用lower将字符串都转换为小写

3.text.split()将字符串按空格划分为单词

4.统计每个单词出现的次数

### 二、启动调试器

我们可以使用Python的内置调试器`pdb`来调试代码。在代码中插入`pdb.set_trace()`，使程序在该位置暂停，等待用户命令：

![image-20240712163622781](/images/image-20240712163622781.png)

引入 pdb

### 三、运行代码并调试

![image-20240712163659720](/images/image-20240712163659720.png)

![image-20240712165034467](/images/image-20240712165034467.png)

n:执行下一步

c:继续执行到结束

p text :打印变量

通过使用 `pdb` 调试器，逐步执行和检查代码，确认 `wordcount` 函数正确实现了单词计数功能。