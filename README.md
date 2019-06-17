# AutoWenJuanXing_spider
todo：问卷星自动填写，未处理验证码，处理ip地址，控制提交时间。

有几个问题：
1、提交答案
#submitdata : 1$3}2$1}3$2}4$1}5$1}6$2}7$3}8$3}9$3}10$4}11$3|4|5}12$2}13$2|4|7|9|11}14$4}15$2

2、对于ip、提交时间 
ip的话可以写一个小爬虫，requests 遍历 3.4段ip地址
提交时间记得sleep、random

3、想想多选怎么处理多选，文本问题目前没有好的解决方法。。。问卷就不放了。。可能会删除。

4、对于答案，小子是根据4年前的相关硕士论文得出的调查数据做的模型
"""
todo:答案，模型 
umm，一共十五道题

模型分析：
1. da学
       师大  内大 农业  工业 财经 
       34%   13％ 21%   17%  15%    

2.年纪分布
因为毕设发布者处于大三 ，因此周围环境为大三，结合参考硕论。
         1  2   3    4
即比例为 19% 21% 37% 23%

3.性别
因为发布者处于师范院校 ，因此男女比例稍偏，结合硕论。
          女  男
即比例为  65% 35％

4.专业属性
发布者处于工科学院，结合整个学校环境，结合硕论。
即
        文科  理科   工科   艺术    其他
        35％  22％   25%   15％    3% 

5.生源地
umm  没有合适的参考，只能根据硕论将城市比例调高
即
  生源地 
        城市  农村
        66%   34%

6.就业形势，近年来就业形势逐渐严峻，结合硕论。
        严峻  正常  容易  不了解
        58%  20%   18%   4％      

7.创业。。。
结合情况，结合硕论 
    创业 不创业
    26%  74%

8.想要的工作单位
结合硕论 
        外企  国企  政府机关  私营民营  自主创业
         28%   25%   35%      9%      3%

9.看中企业什么
结合硕论 
        公司规模  个人发展  待遇  公司名气  对人的重视程度
           20%    25%     28%       9%       18%


10.薪资要求
结合硕论
        3000-   3-6000  6-9000  9－12000 12000+
         1%       66%     21%      8%       4%

11.工作地域
结合硕论 
        沿海发达  内地大  东部中小 西部中小 边远。。
         37％     51%      3%      2％    7%
         
         
12.具有的素质 （最多三个）
   专业水平  心理素质  沟通能力  组织能力  适应能力 品德  
      74％    40%      59%      31%     46%    76%       tol = 326%
yici  23%     12%      18%      9%      14%    24%
      
      
13.影响决策
结合硕论 
        父母  老师  朋友  社会舆论  不受他人影响 其他
        22%   25%   8%      27%         12％    6%

14.影响五因素
结合硕论 
        能力 学历 专业  就业信息 实践经验   户口人口指标 
        57%  65% 48%     52%     84%     43%         tol = 421
        14   15  11      12      20      10
        社会关系 学习成绩 心理素质 
         34%     12%    26%    
         8       3      6
15.就业难的原因 
结合硕论 
        社会需求少 不公平现象 单位挑剔 毕业生挑剔  
        14%        19%      15%      27%
        信息发布不及时 沟通不畅 过度依赖学校 其他
        2%            5％      17%        1%
        
16.就业态度
结合硕论  
        先就业  先择业  考研   待业  创业  其他  
        43%     6%     38％   3%    4%   6%


"""
