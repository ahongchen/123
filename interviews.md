# 面试题收集
## 1，爬虫的爬取时间，每秒爬取数量，总数据量。
## 2，scrapy的结构，scrapy-redis了解吗？
## 3，实现一个单例，使用装饰器实现。
## 4，生成器的原理是什么？
## 5，实现一个单元测试。
## 6，re的常用函数，贪婪非贪婪的区别。
## 7，项目为什么用tornado框架？
## 8，请写出一段Python代码实现删除一个list里面的重复元素，保持列表有序。
## 9，描述关系数据库中的一对一，一对多，多对多，及在django中的使用方式。
## 10，代码实现django中处理一个post表单的验证流程，编写测试用例。
	表单字段：
	```
	name: string(1-50)
	age: int(1-120)
	address: string(2-100字节)
	credit: int(0-100)
	```
## 11，django开发中如何进行model测试，view测试，前端页面测试。
## 12，描述一个django demo项目的开发流程。
## 13，怎么实现session功能。
## 14，举例查询和替换一个文本字符串中的特定文本。
## 15，简述wsgi和uwsgi的作用和关系。
## 16，简单比较一下flask、django和tornado
## 17，编写爬虫的常用模块或者框架有哪些？请说明一个爬虫的行为步骤。
## 18，已知一颗二叉树的先序遍历序列为ABCDEFG，中序遍历为CDBAEGF，能否唯一确定一颗二叉树？如果可以，请画出这颗二叉树。
## 19，排序算法都有哪些？用python写一种排序算法。
## 20，简述一次完整的http通信过程。说明常用的请求方式、响应状态吗有哪些，并解释http的无状态性和对cookies的理解。
## 21，说说进程、线程和锁的关系。
## 22，MySQL操作：
	- 为person表的name属性创建唯一属性。
	- 连表查询A(id,name,age,sex)表中name属性和B(id,book,writer,number)表中writer属性相等的所有数据。
## 23，a = [1,2,'hello',[1,2]]; b1 = a
	b2 = copy.copy(a); b3 = copy.deepcopy(a)
	如果修改a[0] = 2, a[-1].append(0)操作之后，b1，b2，b3之后有什么不同？(从赋值，浅拷贝，深拷贝的内存状态讨论)。
## 24，re的match和search有什么区别？
## 25，django-restful框架了解吗？
## 26，以下操作的时间复杂度是多少？
	```
	list.index
	dict.get
	x in set(...)
	```
## 27，解释以下输出的原因：
	```
	>>>'{:0.2f}'.format(0.135)
	'0.14'
	>>>'{:0.2f}'.format(0.145)
	'0.14'
	```
## 28，简述代码抛出以下异常的原因。
	IndexError, AttributeError, AssertionError, NotImplementedError, StopIteration, TypeError, IndentionError
## 29，简述cookie和session的区别与联系。
## 30，简述什么是浏览器的同源策略。
## 31，git commit --ammend有何用处？
## 32，git如何查看某次提交修改的内容。
## 33，git如何比较两个commit的区别。
## 34，git如何把分支A上某个commit应用到分支B上。
## 35，如何查看linux系统的启动时间，磁盘使用量，内存使用量。
## 36，简述你对GIL的理解。
## 37，简述以下内置函数的用法。
	- reduce，map，any，all
## 38，copy和deepcopy的区别是什么？
## 39，简述多线程，多进程和协程之间的区别。
## 40，代码中经常遇到的*args, **kwargs含义及用法。
## 41，列举一下你知道的HTTP Header及其功能。
## 42，两个列表，提取重复和不重复的元素。
## 43，S1 = u'\xe6\x97\xa0\xe5\x90\x8d'; S2 = '\xe6\x97\xa0\xe5\x90\x8d', 分别在win环境和linux环境下输出为中文.
## 44，分别用xpath beautifulsoup 正则 获取lxml文档中的注释。
```
html_str = """
<div id="box1">this from blog.csdn.net/lncxydjq , DO NOT COPY!
    <div id="box2">*****
        <!--can u get me, bitch?-->
    </div>
</div>
"""
```
## 45，让其输出为中文
```
import requests
url = 'http://xyzfgjj.xys.gov.cn/chaxun_geren.asp'
response = requests.get(url)
print response.text # 乱码
print response.content # 乱码
# 输出如下：
# <td><font color="#ff0000">µ±Ç°Î»ÖÃ£º</font><a href="index.asp">Ê×Ò³
# </a>&nbsp;&gt;&gt;&nbsp;¸öÈËÕÊ»§²éÑ¯</td>
```
## 46，如何在生产环境中 对限定使用ie浏览器 activeX密码登录控件 的银行网站 做网银登录？
## 47，基于tornado写出一个或多个异步协程爬虫demo，展示点：get请求，post请求，获取/更新cookies，设置/获取完整请求头信息。
## 48，用除了python以外的其他语言写个helloworld。
## 49，请列举你所用过的Python代码检测工具。
## 50，简述Python垃圾回收机制及如何解决循环引用。
## 51，简述Python2中什么样的情况下会触发UnicodeDecodeError。
## 52，请选择你认可的代码风格并给出原因。
## 53，请给出下面代码片段的输出。
```
def say_hi(func):
	def wrapper(*args, **kwargs):
		print("Hi")
		ret = func(*args, **kwargs)
		print("Bye")
		return ret
	return wrapper

def say_yo(func):
	def wrapper(*args, **kwargs):
		print("Yo")
		return func(*args, **kwargs)
	return wrapper

@say_hi
@say_yo
def func():
	print("Rock & Roll")

func()
```
## 54，参看上一题代码。
```
@say_hi
@say_yo
def func():
	print("Rock & Roll")
```
请给出不使用装饰器语法糖实现和上面功能一致的代码。
## 55，请看下面代码片段。
```
try:
	raise ValueError("Something wrong!")
except:
	# do something
	raise e
```
请简述若将第5行改为raise会产生哪些变化。
## 56，参考下面代码片段。
```
class Context:
	pass

with Context() as ctx:
	ctx.do_something()
```
请给出Context类的实现代码。
## 57，请列举常见的HTTP头及其作用。
## 58，请列举常见的HTTP状态响应码及其意义。
## 59，请简述对RESTful API设计规范的理解。
## 60，请简述HTTP缓存机制。
## 61，请简述cookie和session之间的关系。
## 62，请给出3个经常访问的技术网站或博客。
## 63，请列举最近关注的一些技术。
## 64，请列举你认为不错的一些技术书籍和你最近在看的书籍（不限于技术）。
## 65，请列举你阅读过源码的一些项目。
## 66，请简述标准库中functools.partial的实现思路。
## 67，请列举常见的MySQL存储引擎。
## 68，InnoDB有哪些特性。
## 69，请列出一些MySQL数据库查询优化的技巧。
## 70，请简述SQL注入的攻击原理及如何在代码层面放置SQL注入。
## 71，请简述MySQL查询时如何关联多张表。
## 72，请给出下面代码片段的输出：
```
def test():
	try:
		raise ValueError("Something wrong!")
	except ValueError as e:
		print("Error occurred!")
	finally:
		print("Done")

test()
```
## 73，请给出下面代码片段的输出
```
class Singleton:
	_instance = None
	def __new__(cls, *args, **kwargs):
		print("New")
		if cls._instance is None:
			print("Create")
			cls._instance = super().__new__(cls, *args, **kwargs)

		return cls._instance

	def __init__(self):
		print("Initialize")
		self.prop = None

s1 = Singleton()
s2 = Singleton()
```
## 74，请简述如何编写清晰可读的代码。
## 75，描述对super，pass，yield，lambda关键字修饰的理解。
## 76，请大致描述一下python的GIL机制，以及python中多线程和多进程的区别。
## 77，python是如何进行内存管理的，以及大致描述一下python的GC机制。
## 78，请分别描述一下类装饰器和函数装饰器的实现过程及应用场景。
## 79，请用两个队列来实现一个栈（给出伪代码即可）。
## 80，实现一个Singleton单例类，要求遵循基本语言编程规范。
## 81，请实现一个简单的socket编程，要求：1），实现server端的功能即可。2），遵循基本语言编程规范。
## 82，请为掌阅设计一个并发处理KEY-VALUE引擎，要求每条请求的数据小于16K，数据总量为1T，QPS为5000/s。
	要求：1），请给出该系统需要配备多少资源，服务器数量，服务器内存大小及硬盘空间等。2），要求系统平滑可扩展，高可用。3），尽可能的降低系统复杂度。
## 83，解释什么是栈溢出，在什么情况下可能出现。
## 84，简述CPython的内存管理机制。
##85，列举你知道的Python的魔法方法及用途。
## 86，已知以下list：
```
list1 = [
	{
	'mm': 2
	},
	{
	'mm': 1
	},
	{
	'mm': 4
	},
	{
	'mm': 3
	},
	{
	'mm': 5
	}
]
```
	1），把list1中的元素按照mm的值排序。
	2），获取list1中第一个mm值等于x的元素。
	3），list1[::4]输出是什么。
	4），删除list1中所有mm等于x的元素，且不对list1重新赋值。
	5），取出list1中mm最大的元素，不能排序。
## 87，redis的数据结构有哪些？
## 88，进程线程间的通信与同步。
## 89，怎样获得访问前10的ip。
## 90，画三次握手，四次挥手。
## 91，list=[1,2,0,2,4,0,5]，不可以再多另一个列表，把0都挪到后面去。
## 92，用python写个二分查找，前提条件：数组array有序，写一个函数找出num（假定num一定在array中）的索引号，比如：L = [1, 4, 12, 45, 66, 99, 120, 444]，需要查找出12。
## 93，select count(*)和select count(1)以及select count(column)的区别？
## 94，请回答以下的输出是多少？如果要得到[0,2,4,6]的结果需要怎么修改？
```
def m():
	return [lambda x:i*x for i in range(4)]
print [f(2) for f in m()]
```
