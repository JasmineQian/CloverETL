<https://www.cnblogs.com/qianjinyan/p/8602425.html>

## 【CloverETL培训】题目
#### 具体要求：

### 导入：

###### 1.在CRM中，创建相应物理表，存储Follow/Binding记录。openid作为逻辑主键
###### 2.Follow/Binding导入相互不影响，一个失败另外一个继续执行
###### 3.Follow中visit为1代表关注，为0代表取关。能够写入CRM的前提是满足ok文件check

   满足批次文件中，关注和取关数据量和ok文件一致。写入后CRM中总关注数和ok文件一致

###### 4.Binding，只要有同名ok文件就做导入CRM操作

 

### 导出：

###### 1.约定日期，和Rolling N两个数字做成可配置.导出文件都是utf-8，txt.文件名中含有YYYYMMDD时间戳
###### 2.Follow分隔符#|#,

   Binding分隔符，同时字段加双引号

  生成Summary_YYYYMMDD.ok文件，必须包含两列内容，导出文件名+包含数量，分隔符tab

  Summary_YYYYMMDD.ok的样例数据：

  Exp_Follow_YYYYMMDD.txt     12120

  Exp_Binding_YYYYMMDD.txt   5598

 

###### 邮件要求：
######  1.一定，一定，一定是要满足，附件提供样例的邮件样式
######  2.邮件内容能够基本说明ETL处理流程中，所涉及到的重要信息，比如处理调用的graph名称，时间点，数据量，异常原因等

 

###### 配置要求：
###### ETL需要整理封装在CLOVER_ETL_TASK/CLOVER_ETL_STEP/CLOVER_ETL_LIST中
