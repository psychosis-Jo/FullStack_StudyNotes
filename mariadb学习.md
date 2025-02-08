# mariadb

## 初始化

```sql
create user "occupation"@"localhost" identified by "Changping@13";
create database occupation default charset utf8 collate utf8_general_ci;
grant all on occupation.* to "occupation"@"localhost";
CREATE TABLE basic (
   occupation_id INT NOT NULL PRIMARY KEY auto_increment COMMENT '职业ID',
   occupation_name VARCHAR(50) NOT NULL COMMENT '职业名称',
   description TEXT COMMENT '该职业的说明和介绍',
   group_id INT NOT NULL COMMENT '分类ID',
   group_name VARCHAR(50) NOT NULL COMMENT '职业分类',
   job_duties TEXT COMMENT '职位或工作的主要责任和职责',
   is_green BOOLEAN DEFAULT FALSE NOT NULL COMMENT '是否为绿色职业(true/false)',
   is_numeric BOOLEAN DEFAULT FALSE NOT NULL COMMENT '是否为数字职业(true/false)',
   is_precondition BOOLEAN DEFAULT FALSE NOT NULL COMMENT '是否有前置条件',
   preconditions ENUM('经验', '资质','both')
) default charset=utf8 COMMENT '第一类_党政机关及社会组织负责人';
```

```sql
INSERT INTO occupation_1 VALUES (1010001, '中国共产党机关负责人', '在中国共产党中央和地方各级机关及其工作机构中，担任领导职务的人员。', 10100, '中国共产党机关负责人', '', 0, 0);
INSERT INTO occupation_1 VALUES (1010002, '中国共产党基层组织负责人
', '在企业、农村、机关、学校、科研院所、街道社区、社会组织等基层单位中国共产党组织中，担任领导职务的人员。', 10100, '中国共产党机关负责人', '', 0, 0);
INSERT INTO occupation_1 
VALUES (1020100, '国家权力机关负责人', '在各级人民代表大会常务委员会及其工作机构中，担任领导职务并具有决策、管理职权的人员。', 10201, '国家权力机关负责人', '1.常务委员会负责人主要处理常务委员会的重要日常工作;\n2.工作机构负责人主要为常务委员会会议和人民代表大会会议服务。', 0, 0);
INSERT INTO occupation_1 
VALUES (1020200, '国家行政机关负责人', '在各级国家行政机关及其工作机构中，担任领导职务并具有决策、管理职权的人员。', 10202, '国家权力机关负责人','1. 领导所属各部门的工作，召集和主持本级行政机关会议；\n2. 签署有关法规、政策、请示、报告、命令等重要文件；\n3. 处理其他日常工作。', 0, 0);
```

## 数据类型

1. 浮点数：float、double、decimal（精准型）
   - decimal：准确的小数值，m是数字总个数（负号不算），d是小数点后个数，m最大值为65，d最大值为30。如`create table t1 (salary decimal(8, 2));` 其中m值为8，d值为2。

```sql
create database unicom default charset utf8 collate utf8_general_ci;
use unicom;
create table admin (
   id int not null auto_increment primary key,
   username varchar(16) not null,
   password varchar(64) not null,
   mobile char(11) not null
) default charset=utf8;
```

## 使用代码执行SQL

1. 在进行增、删、改时，每次execute后必须有commit操作，否则执行不生效；
2. 在查询时执行fetchall/fetchone
   1. fetchone返回的是匹配到的第一条数据，无数据时为空列表
   2. fetchall返回的是所有数据，列表套字典，无数据时为None
3. 对于SQL语句不能使用python的字符串格式化进行拼接（容易被SQL注入），必须使用execute+参数，即`cursor.execute("%s...%s", ["参数1","参数2"])`
