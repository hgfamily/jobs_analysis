智联招聘职位数据挖掘分析
=======================
#项目内容:
---
1.自定义城市：全国31个主要城市  
2.自定义关键词：机器学习  
3.统计分析样本数：6555个  

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
1.数据采集程序说明：  \<br>
调用智联招聘的api爬取智联招聘网上设定城市+职位关键字下所有的职位信息，并将信息存储到本地Mysql保存。  \<br>

2.使用方法：  \<br>
需要在程序中配置Mysql,如：host='localhost',user='root',password='XXX',db='XXX'.  \<br>
Mysql的建表SQL语句如下：  \<br>
CREATE TABLE `机器学习_全国` (  \<br>
  `job_id` int(30) NOT NULL AUTO_INCREMENT,  \<br>
  `职位名称` varchar(255) DEFAULT NULL,  \<br>
  `公司名称` varchar(255) DEFAULT NULL,  \<br>
  `公司链接` varchar(255) DEFAULT NULL,  \<br>
  `职位链接` varchar(255) NOT NULL,  \<br>
  `职位月薪` varchar(255) DEFAULT NULL,  \<br>
  `工作地点` varchar(255) DEFAULT NULL,  \<br>
  `发布日期` varchar(255) DEFAULT NULL,  \<br>
  `工作性质` varchar(255) DEFAULT NULL,  \<br>
  `工作经验` varchar(255) DEFAULT NULL,  \<br>
  `最低学历` varchar(255) DEFAULT NULL,  \<br>
  `招聘人数` varchar(255) DEFAULT NULL,  \<br>
  `职位类别` varchar(255) DEFAULT NULL,  \<br>
  `岗位职责描述` varchar(3000) DEFAULT NULL,  \<br>
  `福利标签` varchar(255) DEFAULT NULL,  \<br>
  PRIMARY KEY (`职位链接`),  \<br>
  UNIQUE KEY `job_id` (`job_id`)  \<br>
) ENGINE=InnoDB  DEFAULT CHARSET=utf8  \<br>

表新建好以后，程序运行时输入：  \<br>
City=全国  \<br>
Keyword=机器学习  \<br>
