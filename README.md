# 2020.8.15 更新
原贴地址：https://www.jianshu.com/p/34961ceedcb4


问卷星反扒机制做出改变。


原博主：在header中加入Referer，Referer内容是问卷网址可以进行问卷填写。但是不能使用X-Forwarded-For，不然会提示点击智能验证。不适用X-Forwarded-For，填写的次数多了也会提示点击只能验证。可以试试加入Referer后使用代理的方式。



小子更换请求头后，再不介入ippool的情况下，无法解决智能验证码。但还是给出更新后的代码。


代码主要在请求头加入referer。此处referer值为问卷url。




# 2020.2.21 更新
分析数据时，相关性回归分析存在问题，使用时请注意








# AutoWenJuanXing_spider
todo：问卷星自动填写，未处理验证码，处理ip地址，控制提交时间。

有几个问题：


1、提交答案
#submitdata : 1$3}2$1}3$2}4$1}5$1}6$2}7$3}8$3}9$3}10$4}11$3|4|5}12$2}13$2|4|7|9|11}14$4}15$2

2、对于ip、提交时间 
ip的话可以写一个小爬虫，requests 遍历 3.4段ip地址。提交时间记得sleep、random

3、想想多选怎么处理多选，文本问题目前没有好的解决方法。。。问卷就不放了。。可能会删除。

4、对于答案，小子是根据4年前的相关硕士论文得出的调查数据做的模型，模型.py里面自己分析吧。。
