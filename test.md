#一节标题
##二节标题

前面是不能用空行吗？前面是不能用空行吗？前面是不能用空行吗？
前面是不能用空行吗？前面是不能用空行吗？前面是不能用空行吗？
前面是不能用空行吗？前面是不能用空行吗？前面是不能用空行吗？

用了空行或制表符缩进会怎么样？用了空行或制表符缩进会怎么样？
用了空行或制表符缩进会怎么样？用了空行或制表符缩进会怎么样？

 用了空行或制表符缩进会怎么样？用了空行或制表符缩进会怎么样？
用了空行或制表符缩进会怎么样？用了空行或制表符缩进会怎么样？

##这是一个引用示例

>这是一个引用的示例
这是一个引用的示例
这是一个引用的示例
这是一个引用的示例
>

#下面是讲列表的（列表时常需要空格）

##这是一个列表

+ 无序列表*+-
+ 无序列表*+-
+ 无序列表*+-

##这是一个有序列表

>数字及数字的顺序没关系

1. 有序列表
2. 有序列表2
3. 有序列表3

>列表项目可以包含多个段落，每个项目下的段落都必须缩进4个空格或是1个制表符
>难道这就是段落不让缩进的原因？

1.  This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

2.  Suspendisse id sem consectetuer libero luctus adipiscing.

>当然，项目列表很可能会不小心产生，例如下面的写法

1986. What a great season.

>换句话说，也就是在行首出现数字-句点-空白，要避免这样的状况，你可以在句点前面加上反斜杠。

1986\. What a great season.



#代码区块

和程序相关的写作或是标签语言原始码通常会有已经排版好的代码区块，通常这些区块我们并不希望它以一般段落文件的方式去排版，而是照原来的样子显示，Markdown 会用 <pre> 和 <code> 标签来把代码区块包起来。

要在 Markdown 中建立代码区块很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以,是每行都缩进，并不是首行。
一个代码区块会一直持续到没有缩进的那一行（或是文件结尾）。

>这是一个普通段落：

>    这是一个代码区块。

Markdown 会转换成：
> <p>这是一个普通段落：</p>

> <pre><code>这是一个代码区块。
> </code></pre>

#分割线

你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：

****

#区块元素

##链接

*下面是行内式写法*

this is [百度](http://www.baidu.com/ "baidu") inline link.

	<p>this is [百度](http://www.baidu.com/ "baidu") inline link.</p>
	<p>此是用code格式写的</p>

*下面是参考式的链接写法，这种简洁点*

I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"

##强调

1. 用*和_为标记，把要强调的内容发到两者之间，使用两个**或两个__会被转成<strong>
2. 用什么开始标记，就用什么结束，不能混用。
3. 可用反斜杠，画成普通的型号或下划线

反引号是代码区段! 'printf()'


##自动链接

<http://google.com/>