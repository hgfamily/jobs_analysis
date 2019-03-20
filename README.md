机器学习职位数据挖掘分析
=======================
#项目内容:
---
1.统计城市：全国31个主要城市  
2.统计关键词：机器学习  
3.统计分析样本数：6555个  
4.数据来源：智联招聘  

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
1.数据采集  
2.数据清洗与处理  
3.数据分析  
4.数据可视化

#项目文件目录
---
* ml_table.sql->数据库建表脚本  
* ml_jobs.csv->数据集  
* dataset.py->数据采集程序  
* jobs_analysis.ipynb->数据分析程序(可直接打开查看数据分析过程和结果)  

#文件说明及使用方法
---
-------------------
* 数据采集程序说明：  
	* 调用智联招聘的api爬取智联招聘网上设定城市+职位关键字下所有的职位信息，并将信息存储到本地Mysql保存。  
* 使用方法：  
* 需要在程序中配置Mysql相关字段,如：host='localhost',user='***',password='***',db='***'.
* 使用数据库建表脚本ml_table.sql创建'机器学习_全国'表
* 表新建好以后，程序运行时输入：  
	* 工作城市=全国  
	* 关键词=机器学习  
* 程序语言及数据库版本:Python 3.5.2、Mysql 5.6.36  

--------------------
* 数据分析程序需要在Anaconda 4.2.0 (64-bit)	环境中运行,该环境保存程序每一步的注释及其运行结果  

--------------------
