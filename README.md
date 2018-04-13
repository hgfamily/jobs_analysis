智联招聘职位数据挖掘分析
=======================
#项目内容:
---
1.自定义城市：全国31个主要城市\<br>
2.自定义关键词：机器学习\<br>
3.统计分析样本数：6555个\<br>

#项目目的:
---
1.不同工作城市的招聘数量分布情况分析
2.不同工作经验的招聘数量分布情况分析
3.工作经验对于收入的影响情况分析
4.工作城市对于收入的影响情况分析
5.招聘数量与学历的关联情况分析
6.学历对于收入的影响情况分析
7.学历与工作经验对于收入的影响情况分析

#项目步骤:
---
1.数据采集：python抓取智联招聘网职位数据
2.数据清洗与处理
3.数据分析
4.数据可视化：柱状图，饼图

----------------------------------
1.数据采集程序说明：
调用智联招聘的api爬取智联招聘网上设定城市+职位关键字下所有的职位信息，并将信息存储到本地Mysql保存。

2.使用方法：
需要在程序中配置Mysql,如：host='localhost',user='root',password='XXX',db='XXX'.
Mysql的建表SQL语句如下：
CREATE TABLE `机器学习_全国` (
  `job_id` int(30) NOT NULL AUTO_INCREMENT,
  `职位名称` varchar(255) DEFAULT NULL,
  `公司名称` varchar(255) DEFAULT NULL,
  `公司链接` varchar(255) DEFAULT NULL,
  `职位链接` varchar(255) NOT NULL,
  `职位月薪` varchar(255) DEFAULT NULL,
  `工作地点` varchar(255) DEFAULT NULL,
  `发布日期` varchar(255) DEFAULT NULL,
  `工作性质` varchar(255) DEFAULT NULL,
  `工作经验` varchar(255) DEFAULT NULL,
  `最低学历` varchar(255) DEFAULT NULL,
  `招聘人数` varchar(255) DEFAULT NULL,
  `职位类别` varchar(255) DEFAULT NULL,
  `岗位职责描述` varchar(3000) DEFAULT NULL,
  `福利标签` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`职位链接`),
  UNIQUE KEY `job_id` (`job_id`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8

表新建好以后，程序运行时输入：
City=全国
Keyword=机器学习
