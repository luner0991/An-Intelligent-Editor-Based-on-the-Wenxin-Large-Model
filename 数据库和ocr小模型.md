## 三、数据库
### 1、简介
   数据库简称 DB，是按照数据结构来组织、存储和管理数据的仓库，用户可以对文件的数据进行增加、删除、修改、查找等操作。
  区分一下，[数据库管理系统](https://so.csdn.net/so/search?q=%E6%95%B0%E6%8D%AE%E5%BA%93%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F&spm=1001.2101.3001.7020)简称DBMS，是一种操纵和管理数据库的大型软件，是用于建立、使用和维护数据库（DB）。它对数据库进行统一的管理和控制，以保证数据库的安全性和完整性。
### 2、为什么要用数据库

1. 数据库可以存储大量的数据信息，方便用户进行有效的访问。数据库还可以对数据进行分类保存，并且能够提供快速的查询。
2. 数据库可以满足应用的共享和安全方面的要求，把数据放在数据库中在很多情况下也是出于安全的考虑。
3. 数据库技术能够方便智能化地分析，产生新的有用信息。
### 3、数据库的分类
**①、关系型数据库**
采用了关系模型来组织数据的数据库，其以行和列的形式存储数据，以便于用户理解，关系型数据库这一系列的行和列被称为表，一组表组成了数据库。下面是常见的一些关系型数据库：
**MySQL:**
免费的数据库系统。被广泛用于**中小型应用系统。体积小、速度快、总体拥有成本低，开放源代码**。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717663646400-397ea6eb-f287-4c82-b8dc-4083eb2dad30.png#averageHue=%23fdf8f1&clientId=u34cee643-dda7-4&from=paste&height=560&id=ua9cd38bc&originHeight=840&originWidth=1404&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=264038&status=done&style=none&taskId=ubf844ccd-4c2b-478a-a4df-1382bfd1958&title=&width=936)

**SQL Server :**
是由微软公司开发的一种[关系型数据库](https://so.csdn.net/so/search?q=%E5%85%B3%E7%B3%BB%E5%9E%8B%E6%95%B0%E6%8D%AE%E5%BA%93&spm=1001.2101.3001.7020)管理系统（RDBMS），用于存储和检索数据。它提供了一个可扩展的、安全的和可靠的数据存储和管理解决方案。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717663693592-daf3ba66-c03c-411e-a443-2cd5db471524.png#averageHue=%23edebeb&clientId=u34cee643-dda7-4&from=paste&height=467&id=udfb38e41&originHeight=700&originWidth=1608&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=565905&status=done&style=none&taskId=ua22712a2-fe96-4fcf-bfe6-65728ab2233&title=&width=1072)
**Oracle：**
是目前比较成功的关系型数据库管理系统。运行稳定、功能齐全、性能超群、技术领先。主要应用在大型的企业数据库领域。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717663723617-aa1e7e99-b1de-45ea-90fd-bb335ab5b366.png#averageHue=%23f9ecea&clientId=u34cee643-dda7-4&from=paste&height=416&id=ua25c2a80&originHeight=624&originWidth=1443&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=135379&status=done&style=none&taskId=ud3be68b0-a6a1-4f41-8263-d1042b568dc&title=&width=962)
### 4、MySQL基本操作详解
上一篇教程已经安装好了MySQL还有phpMyAdmin，直接在这里进行操作。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717665060808-a779175d-8c8d-46c4-bc78-35749822a033.png#averageHue=%23e2c090&clientId=ubfdb1111-5ea0-4&from=paste&height=626&id=ud2a48b5d&originHeight=939&originWidth=1186&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=134205&status=done&style=none&taskId=ub2c423bb-28ed-4fca-bbc0-c61bb4c2bcd&title=&width=790.6666666666666)
右上角点击数据库工具->打开->选择phpMyAdmin，打开网页,账号和密码都是root，登录进去。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717665177926-59923e22-4bbb-4d96-a61b-431fe97e0250.png#averageHue=%23fcfbfb&clientId=ubfdb1111-5ea0-4&from=paste&height=567&id=u96f6f735&originHeight=851&originWidth=1993&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=127501&status=done&style=none&taskId=u5ecab8e5-4de0-4a70-b243-6ddfacb60c4&title=&width=1328.6666666666667)
直接选择SQL，就可以在这里编写SQL语句进行测试了。![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717665254848-26d72c66-256b-4273-8ca3-d4ca4660dbf5.png#averageHue=%23f2f2f1&clientId=ubfdb1111-5ea0-4&from=paste&height=593&id=u9e9081e9&originHeight=890&originWidth=2555&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=228259&status=done&style=none&taskId=u2334abf2-d299-476b-b00f-11b271e411b&title=&width=1703.3333333333333)
#### 4.1、数据库操作
①、查看MySQL服务器下所有数据库
```sql
SHOW DATABASES;
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717665548932-32c6c838-4784-4a28-8e67-3d3f8d535d5b.png#averageHue=%23f0efef&clientId=ubfdb1111-5ea0-4&from=paste&height=468&id=u6256a5d8&originHeight=702&originWidth=2198&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=132535&status=done&style=none&taskId=u8af625aa-0981-402f-a3a3-3c520cdf29a&title=&width=1465.3333333333333)
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717665569661-f608cf39-575b-4146-b091-5d81529068b2.png#averageHue=%23f0efef&clientId=ubfdb1111-5ea0-4&from=paste&height=475&id=u8654678b&originHeight=713&originWidth=1831&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=148640&status=done&style=none&taskId=u0486836a-3a53-41b4-8de5-a4087c5e6e4&title=&width=1220.6666666666667)
> information_schema数据库是MySQL服务器的数据字典（保存所有数据表和库的结构信息）
> performance_schema数据库是MySQL服务器的性能字典（保存全局变量等的设置）
> mysql 主要负责MySQL服务器自己需要使用的控制和管理信息（用户的权限关系等）
> sys是系统数据库，包括了存储过程，自定义函数等信息
> 这4个数据库是MySQL安装时自动创建的，建议不要随意的删除和修改这些数据库，避免造成服务器故障。

②、查看指定数据库的创建信息
```sql
SHOW CREATE DATABASE 数据库名称;
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717665736897-0eef1f94-160b-4691-b558-7cf956164530.png#averageHue=%23f1f4e5&clientId=ubfdb1111-5ea0-4&from=paste&height=210&id=ud31570ae&originHeight=315&originWidth=1363&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=29585&status=done&style=none&taskId=u107d38ce-505d-45bd-8ac5-2ae29f5c3d5&title=&width=908.6666666666666)
> 显示sys数据库的SQL语句，以及数据库的默认字符集

③、选择数据库并查看当前数据库
**切记**：在输入当前数据库查询的SQL语句前，必须先选择数据库。
先选择editdata数据库,执行如下语句：
```sql
USE EditData
```
接着查看当前数据库：
```sql
SELECT DATABASE();
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717666197601-7b97c35c-01b7-4499-a7a6-4c8548e09ed0.png#averageHue=%23f1f0f0&clientId=ubfdb1111-5ea0-4&from=paste&height=457&id=uc6dc8003&originHeight=686&originWidth=2189&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=124038&status=done&style=none&taskId=u4916ca9b-17d5-4868-8f1a-7a24fd99f83&title=&width=1459.3333333333333)
④、创建数据库
```sql
CREATE DATABASE IF NOT EXISTS userinfo;
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717669478094-a0b92bd4-881f-4ec2-b822-6c784459b5e1.png#averageHue=%23ecece3&clientId=ubfdb1111-5ea0-4&from=paste&height=293&id=u9fb2229d&originHeight=293&originWidth=1906&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=59679&status=done&style=none&taskId=u1b0550cd-aeb6-49e6-a13a-ef67ed4c7f6&title=&width=1906)
⑤、选择数据库
```sql
USE userinfo;
```
也可以点击左侧的数据库列表进行数据库的选择。
⑥、删除数据库
```sql
DROP DATABASE IF EXISTS userinfo;
```

- 删除数据库，清除数据库中的所有数据，回收为分配的存储空间。
- 在执行DROP DATABASE 删除数据库时，若待删除的数据库不存在，MySQL服务器会报错。
- 若想避免上述的情况，在进行删除数据库操作时，使用IF EXISTS来进行规避待删除的数据库不存在报错情况。
#### 4.2、数据表操作
①、创建数据表
```sql
CREATE [TEMPORARY] TABLE [IF NOT EXISTS] 表名( 
    字段1 字段1类型 [字段属性] [COMMENT 字段1注释 ], 
    字段2 字段2类型 [字段属性] [COMMENT 字段2注释 ], 
    字段3 字段3类型 [字段属性] [COMMENT 字段3注释 ],
    ...... 
    字段n 字段n类型 [COMMENT 字段n注释 ] 
) [表属性] [ COMMENT 表注释 ] ;
```
例子，创建一个user的表，存储用户的用户名和密码。
```sql
CREATE TABLE `userinfo`.`user` ( 
  `id` INT NOT NULL AUTO_INCREMENT , 
  `username` VARCHAR(200) NOT NULL ,
  `password` VARCHAR(200) NOT NULL , 
  PRIMARY KEY (`id`)) ENGINE = MyISAM;
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717669948734-6768b2c2-86bc-49f0-af0a-800e29bc7388.png#averageHue=%23f1f1f1&clientId=ubfdb1111-5ea0-4&from=paste&height=456&id=u5914a38c&originHeight=456&originWidth=1674&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=61865&status=done&style=none&taskId=u99bedc75-f5d7-4641-98a1-cf9e23048e6&title=&width=1674)
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717669962706-199b786f-becd-4cfa-831d-eef59e5af4cd.png#averageHue=%23eeeeed&clientId=ubfdb1111-5ea0-4&from=paste&height=393&id=u142b97af&originHeight=393&originWidth=1900&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=75765&status=done&style=none&taskId=ud5fc8fb2-b93a-49df-8d26-4dd27ec6472&title=&width=1900)
②、查看数据表
```sql
SHOW TABLES;
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717670175058-81dbda48-c3bf-4c1f-8ef6-fbc64a2dce1c.png#averageHue=%23f4f6e8&clientId=ubfdb1111-5ea0-4&from=paste&height=216&id=u358b78d1&originHeight=216&originWidth=693&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=9142&status=done&style=none&taskId=u5c0459fb-5379-46c9-8a7b-7bb1bd4b5ce&title=&width=693)
③、查看数据表的相关信息
```sql
SHOW TABLE STATUS FROM 数据库名;
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717670250553-bf838050-e44f-4aeb-a4a3-71b5e667ae98.png#averageHue=%23f2f3e5&clientId=ubfdb1111-5ea0-4&from=paste&height=234&id=ub68d1ef7&originHeight=234&originWidth=1670&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=33893&status=done&style=none&taskId=u6247eb20-14ac-49e6-99f0-a03615981b5&title=&width=1670)
④、查看表结构
```sql
{DESCRIBE|DESC} 数据表名;
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717670327106-40b7c07f-42b2-4f0f-9b48-4ad643b9f835.png#averageHue=%23f4f5e9&clientId=ubfdb1111-5ea0-4&from=paste&height=251&id=ud7372e96&originHeight=251&originWidth=816&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=18691&status=done&style=none&taskId=u04179431-9c2c-410a-b162-2c7ddb05595&title=&width=816)
⑤、修改数据表名称
```sql
ALTER TABLE 旧表名 RENAME [TO|AS] 新表名;
```
例如:
```sql
ALTER TABLE user RENAME AS users;
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717670481397-028af88f-d263-4544-80e4-0e712de6ebdc.png#averageHue=%23ecede4&clientId=ubfdb1111-5ea0-4&from=paste&height=313&id=ufa10d425&originHeight=313&originWidth=1374&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=56615&status=done&style=none&taskId=uaa71f333-f611-47d7-b1c9-454e48b4c53&title=&width=1374)
⑥、删除数据表
```sql
DROP [TEMPORARY] TABLE [IF EXISTS] 数据表1;
```
例如:
```sql
DROP TABLE IF EXISTS users;
```
就成功删除了
#### 4.3、数据操作
①、增加数据
为了方便操作，这里重新加上刚删除的表。
```sql
CREATE TABLE `userinfo`.`user` ( 
  `id` INT NOT NULL AUTO_INCREMENT , 
  `username` VARCHAR(200) NOT NULL ,
  `password` VARCHAR(200) NOT NULL , 
  PRIMARY KEY (`id`)) ENGINE = MyISAM;
```
可以为部分字段添加数据，模板：
```sql
INSERT [INTO] 数据表名(字段名1,字段名2,...,字段名n) {VALUES|VALUE} (值1,值2,...,值n);
```
例如：
```sql
INSERT INTO user(`username`,`password`) VALUES("123","123");
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717671089011-c4e41c3f-3e50-4191-998d-39523e04fa57.png#averageHue=%23e9f6a3&clientId=ubfdb1111-5ea0-4&from=paste&height=169&id=ud343469c&originHeight=169&originWidth=1676&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=13928&status=done&style=none&taskId=u92b1e710-a6e9-4b5b-8578-ae7a68885c3&title=&width=1676)
也可以用下面的方式:
```sql
INSERT [INTO] 数据表名 SET 字段名1 = 值1 [,字段名2 = 值2,...,字段名n = 值n]
```
例如:
```sql
INSERT INTO user SET `username` ="1234" ,`password`="1234";
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717671244656-34f263ca-0774-4116-af00-769c400de32f.png#averageHue=%23f3f6df&clientId=ubfdb1111-5ea0-4&from=paste&height=208&id=u46368584&originHeight=208&originWidth=893&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=9886&status=done&style=none&taskId=u01aa2d5e-2074-467f-9e5a-db9ebd66c39&title=&width=893)
为所有字段添加数据。
```sql
INSERT [INTO] 数据表名 {VALUES|VALUE} (值1,值2,...,值n);
```
例如:
```sql
INSERT INTO user VALUES ("3","12345","12345");
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717671350199-0fdd3b5e-8649-405e-9a01-811d667c57de.png#averageHue=%23e8f6a2&clientId=ubfdb1111-5ea0-4&from=paste&height=107&id=uf36ebdb7&originHeight=107&originWidth=755&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=5795&status=done&style=none&taskId=u6da21be3-83af-4a3d-af28-240f3608125&title=&width=755)
在为所有字段添加数据时，可以省略字段名称，严格按照数据表结构（字段的位置）插入对应的值。
INTO 为可选择项；VALUE 和VALUES可以任选一种，通常情况下使用VALUES；值列表中值之间用逗号隔开。
在插入数据时，插入的数据顺序必须与创建数据表时对应的字段位置顺序相同，不可搞乱顺序，规避数据顺序错误情况。
②、查询数据
**查询全部数据**
```sql
SELECT * FROM 数据表名;
```
例如查询user所有的数据：
```sql
SELECT * FROM user;
```
可以查询出所有内容。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717671511810-04223c2a-658d-49c6-a942-984163b0da87.png#averageHue=%23e7f1a0&clientId=ubfdb1111-5ea0-4&from=paste&height=368&id=u21f417f1&originHeight=368&originWidth=789&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=25162&status=done&style=none&taskId=u11ebcff7-adad-41fc-8d35-5cd9c1e17fd&title=&width=789)
**查询表子部分字段**
```sql
SELECT {字段名1,字段名2,字段名3,...,字段名n} FROM 数据表名;
```
例如只查询用户名可以这样写:
```sql
SELECT username FROM user;
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717671688162-1b1e9856-1c66-430a-8657-b5b1de988955.png#averageHue=%23f6f7ec&clientId=ubfdb1111-5ea0-4&from=paste&height=275&id=ubff77655&originHeight=275&originWidth=615&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=13502&status=done&style=none&taskId=u06559e10-caa0-46fb-a853-e27f2f121cc&title=&width=615)
**简单条件查询数据**
```sql
SELECT * FROM 数据表名 WHERE 条件表达式;
```
例如:
```sql
SELECT *  FROM user WHERE `username` = "123";
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717671813425-eff53555-fe65-4e32-90de-6b98a8f913a4.png#averageHue=%23e8f2a0&clientId=ubfdb1111-5ea0-4&from=paste&height=336&id=u1a5ff324&originHeight=336&originWidth=840&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=23847&status=done&style=none&taskId=uca677560-fe7d-490a-824c-7427a50e98c&title=&width=840)
```sql
SELECT *  FROM user WHERE `username` = "123" and `password`="123";
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717671860772-a2f7a5b7-5d4b-45fc-84b2-6adb3b8f617b.png#averageHue=%23e8f2a0&clientId=ubfdb1111-5ea0-4&from=paste&height=334&id=ue2402cc4&originHeight=334&originWidth=924&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=24977&status=done&style=none&taskId=u17d83afc-b718-490a-8f17-c20f1981819&title=&width=924)
③、更新数据
```sql
UPDATE 数据表名 SET 字段名1 = 值1 [,字段名2 = 值2,...] [WHERE 条件表达式];
```
例如:
```sql
UPDATE user SET `username` = "666" ,`password` ="666" WHERE `id`="1";
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717672023339-99b44277-c465-4b4c-a034-2b7c2df9813c.png#averageHue=%23e8f5a2&clientId=ubfdb1111-5ea0-4&from=paste&height=159&id=u00ab6f71&originHeight=159&originWidth=656&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=7310&status=done&style=none&taskId=u0f5f9926-9ebf-401c-b61a-d8339a3077a&title=&width=656)
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717672036015-d3b80ea0-74db-4bce-8c16-73c40fbf3279.png#averageHue=%23f6f4f3&clientId=ubfdb1111-5ea0-4&from=paste&height=136&id=u4344ab66&originHeight=136&originWidth=548&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=14526&status=done&style=none&taskId=udc31cc36-2f40-438c-bb03-53d40d96a49&title=&width=548)
④、删除数据
```sql
DELETE FROM 数据表名 [WHERE 条件表达式];
```
例如：
```sql
DELETE FROM user WHERE `username`="1234";
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717672158583-105425bc-ae5a-4322-9015-4d622d856545.png#averageHue=%23f2f5e1&clientId=ubfdb1111-5ea0-4&from=paste&height=164&id=u71127eb8&originHeight=164&originWidth=837&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=7596&status=done&style=none&taskId=u76a6444a-bc1c-4791-9d46-6db3acd4926&title=&width=837)
### 5、pymysql基本操作
#### 5.1、pymysql介绍
PyMySQL是一个Python编写的MySQL驱动程序,让我们可以用Python语言操作MySQL数据库。
#### 5.2、数据操作
首先创建好数据库，userinfo在上面练习过程中创建好了，以这个为例。
接着编写测试函数进行数据操作的增删改查，在之前的后端项目创建一个test.py文件进行测试。
①、增加数据
```sql
import pymysql

def adduser():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    username="555"
    password="555"
    sql = "insert into user (`username`, `password`)values('" + str(username) + "','" + str(password) + "');"
    print(sql)

    count = cursor.execute(sql)
    print(count)
    conn.commit()
    cursor.close()
    conn.close()
    return "success"


if __name__ == '__main__':
    adduser()

```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717673390242-49aa367a-7d4d-4107-8073-3d8ac475ba7e.png#averageHue=%23212226&clientId=ubfdb1111-5ea0-4&from=paste&height=189&id=uf09cd13f&originHeight=189&originWidth=1151&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=24730&status=done&style=none&taskId=u27bdc827-2a77-4615-ad0d-b5183f97265&title=&width=1151)
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717673399816-5a1a7f90-6526-4383-ac94-1f42b07faef7.png#averageHue=%23f3f3e9&clientId=ubfdb1111-5ea0-4&from=paste&height=306&id=ub79bcff6&originHeight=306&originWidth=505&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=22359&status=done&style=none&taskId=uc9f8f62d-5cf5-4c15-88c9-8a11f645cd2&title=&width=505)
②、查询所有数据
```sql
import pymysql

def adduser():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    username="555"
    password="555"
    sql = "insert into user (`username`, `password`)values('" + str(username) + "','" + str(password) + "');"
    print(sql)

    count = cursor.execute(sql)
    print(count)
    conn.commit()
    cursor.close()
    conn.close()
    return "success"

def serchall():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    sql = "select * from user;"
    count = cursor.execute(sql)
    data = cursor.fetchall()  # cursor.fetchall()
    tableData = []
    for i in range(count):
        datai = data[i]
        dataiJson = {"id": datai[0], "username": datai[1], "password": datai[2]}
        tableData.append(dataiJson)
    conn.commit()
    cursor.close()
    conn.close()
    return tableData


if __name__ == '__main__':
    tableData=serchall();
    print(tableData)
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717673599528-ba0dab4c-0697-4ae3-9e9d-5ec8412904d9.png#averageHue=%23202225&clientId=ubfdb1111-5ea0-4&from=paste&height=208&id=u27bfbeff&originHeight=208&originWidth=2382&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=33753&status=done&style=none&taskId=u0e065f84-b623-49f9-bfdf-5b4bf464d67&title=&width=2382)
③、删除数据
```sql
import pymysql

def adduser():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    username="555"
    password="555"
    sql = "insert into user (`username`, `password`)values('" + str(username) + "','" + str(password) + "');"
    print(sql)

    count = cursor.execute(sql)
    print(count)
    conn.commit()
    cursor.close()
    conn.close()
    return "success"

def serchall():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    sql = "select * from user;"
    count = cursor.execute(sql)
    data = cursor.fetchall()  # cursor.fetchall()
    tableData = []
    for i in range(count):
        datai = data[i]
        dataiJson = {"id": datai[0], "username": datai[1], "password": datai[2]}
        tableData.append(dataiJson)
    conn.commit()
    cursor.close()
    conn.close()
    return tableData

def deletedata():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    username="555"
    sql= "delete from user where username='"+str(username)+"';"
    count=cursor.execute(sql)
    print(count)
    conn.commit()
    cursor.close()
    conn.close()
    return "success"


if __name__ == '__main__':
    deletedata()
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717673792104-e2135156-1aba-4107-bc0f-a9859b4a8358.png#averageHue=%23f2f3ea&clientId=ubfdb1111-5ea0-4&from=paste&height=291&id=uba1d2e94&originHeight=291&originWidth=1070&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=43290&status=done&style=none&taskId=u25d0d812-710d-49a4-bdb0-347843b6324&title=&width=1070)
④、修改数据
```sql
import pymysql

def adduser():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    username="555"
    password="555"
    sql = "insert into user (`username`, `password`)values('" + str(username) + "','" + str(password) + "');"
    print(sql)

    count = cursor.execute(sql)
    print(count)
    conn.commit()
    cursor.close()
    conn.close()
    return "success"

def serchall():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    sql = "select * from user;"
    count = cursor.execute(sql)
    data = cursor.fetchall()  # cursor.fetchall()
    tableData = []
    for i in range(count):
        datai = data[i]
        dataiJson = {"id": datai[0], "username": datai[1], "password": datai[2]}
        tableData.append(dataiJson)
    conn.commit()
    cursor.close()
    conn.close()
    return tableData

def deletedata():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    username="555"
    sql= "delete from user where username='"+str(username)+"';"
    count=cursor.execute(sql)
    print(count)
    conn.commit()
    cursor.close()
    conn.close()
    return "success"
def update():
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use userinfo')
    psd="789"
    sql= """
    update user set `username`='"""+str("789")+"', `password`='"+str(psd)+"' where `username`='"+str("12345")+"';"
    count=cursor.execute(sql)
    print(count)
    conn.commit()
    cursor.close()
    conn.close()
    return "success"

if __name__ == '__main__':
    update()
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717674080305-2eeb3331-46db-43ec-a5d0-12e221a9992a.png#averageHue=%23f0efee&clientId=ubfdb1111-5ea0-4&from=paste&height=99&id=uea0b2cc2&originHeight=99&originWidth=745&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=15188&status=done&style=none&taskId=ubabae71c-c114-47b7-ab55-0498b8f2c38&title=&width=745)
## 四、OCR识别
OCR识别，是一种通过扫描、拍照等光学输入方式将各种票据、报刊、书籍、文稿及其他印刷品的文字转化为图像信息，再利用文字识别技术将图像信息转化为可以编辑和检索的文本的技术。OCR识别技术在现代社会中发挥着重要作用，它极大地提高了数据输入的效率和准确性，为文档处理和信息管理提供了高效的解决方案。本章节将详细阐述如何结合PaddlePaddle框架，实现前后端协同工作以完成输入图像中的文字识别任务。
### 1、图片上传
为了进行OCR操作，首先需要实现让用户在前端上传图片，这里使用Elemet-Plus的Upload组件进行实现。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717212870158-e47f67b5-b432-4d23-acb9-bc057cf49492.png#averageHue=%23a4ab7a&clientId=ua37b745e-0d34-4&from=paste&height=899&id=ub39a9454&originHeight=1349&originWidth=2497&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=324329&status=done&style=none&taskId=u0c5c5c13-d6be-4a1f-836e-1bb2defbcf9&title=&width=1664.6666666666667)
先简单调整一下前端样式，打开src/style.css,修改#app样式如下:
```css
#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
  text-align: center;
}
```
在HomePage/index.vue中进行测试，修改代码如下。
```vue
<template>
  <div class="mainbody">
    <h1 class="headtitle">首页</h1>
    <div>
      <h2 class="">{{ demoStore.helloPinia}}</h2>
    </div>
    
    <div class="uploadimage">
      <p class="commodity_img">
            <!-- 上传图片
              :class="boxdisplay"
             -->
            <el-upload
              :on-success="handleSuccess"
              list-type="picture-card"
              :auto-upload="false"
              :on-change="handleChanges"
              :before-remove="beforeRemove"
              :on-preview="handlePictureCardPreview"
              :file-list="fileList "
              multiple
              limit="1"
              name="img"
            >
              <el-icon class="avatar-uploader-icon">
                <Plus />
              </el-icon>
            </el-upload>
        </p>

    <el-dialog v-model="dialogVisible">
      <img w-full class="imageshow" :src="dialogImageUrl" alt="Preview Image" />
    </el-dialog>
  </div>
  <el-button type="primary" @click="uploadimg">上传图片</el-button>
  </div>
</template>
<script setup lang="ts">
  import { mainStore} from '../../store/index'
  /* 引入storeToRefs */
  import { storeToRefs } from 'pinia'

  //storeToRefs只会关注sotre中数据，不会对方法进行ref包裹

  /* 得到countStore */
  const demoStore =mainStore()

  import axios from 'axios'
  //进行测试接口调用
  const adduser=()=>{
    let formData = new FormData();
    formData.append("username","12345");
    formData.append("password","54321");
    let url = 'http://127.0.0.1:5000/adduser' //访问后端接口的url
    let method = 'post'
    axios({
      method,
      url,
      data: formData,
    }).then(res => {
      // alert(res.data)
      console.log("你好")
    });
  }
  adduser()

  import { ref } from 'vue'
  import { ElMessage } from 'element-plus';
  import { Delete, Download, Plus, ZoomIn } from '@element-plus/icons-vue'

  import type { UploadFile } from 'element-plus'

  const dialogImageUrl = ref('')
  const dialogVisible = ref(false)
  const disabled = ref(false)

  const handleRemove = (file: UploadFile) => {
    file.url = '';
    file=null;
  }

  const handlePictureCardPreview = (file: UploadFile) => {
    dialogImageUrl.value = file.url!
    dialogVisible.value = true
  }

  const handleDownload = (file: UploadFile) => {
   
  }

  const boxdisplay = ref("show_box");

  const upload_btn = ref(false);
  const fileList = ref([]);
  const handleSuccess = () => {
    // 上传成功后，隐藏上传按钮
    upload_btn.value = true;
  };
  const handleChanges = img => {
    fileList.value.push(img);
    boxdisplay.value = "hide_box";
  };
  import {ElMessageBox} from 'element-plus'
  // 删除
  const beforeRemove = () => {
    const result = new Promise((resolve, reject) => {
      ElMessageBox.confirm("此操作将删除该图片, 是否继续?", "提示", {
        confirmButtonText: "确定",
        cancelButtonText: "取消",
        type: "warning"
      })
        .then(() => {
          boxdisplay.value = "show_box";
          resolve();
          fileList.value = [];
          upload_btn.value = false;
        })
        .catch(() => {
          reject(false);
        });
    });
    return result;
  };
  const uploadimg = () => {
    // alert("上传图片")
    let formData = new FormData();
      // 遍历fileList，为每个文件创建一个新的表单字段 
    formData.append("username","12345");
    fileList.value.forEach((file, index) => {  
      // 假设后端期望的文件字段名为 'file[]' 以支持多文件上传  
      // 如果后端只期望单个文件，则字段名可能只是 'file'  
      // formData.append(`file[${index}]`, file.raw);  
      formData.append("file",file.raw);
      console.log(file.raw)
    });  

    let url = 'http://127.0.0.1:5000/uploadimages' //访问后端接口的url
    let method = 'post'
    axios({
        method,  
        url,  
        data: formData,  
        headers: {  
          'Content-Type': 'multipart/form-data' // 确保设置了正确的Content-Type  
        }  
    }).then(res => {
        const result = new Promise((resolve, reject) => {
                resolve();
                fileList.value = [];
                upload_btn.value = false;
                ElMessage({ message: '图片上传成功', type: 'success' });  
              })
              .catch(() => {
                reject(false);
              });
          });
  }
</script>

<style scoped>
.mainbody {
  position: relative;
  width:100vw;
  height: 100vh;
  display: block;
}
.headtitle {
  filter: drop-shadow(0 0 2em #646cffaa);
  margin: 0;
}
</style>
<style lang="scss" scoped>
/* #在此处编写代码 */
.mainbody{
  background: #76cfe5;
}
</style>
<style scoped>
.hide_box  {
  display: none;
}
.show_box{
  display: inline-flex;
}
.imageshow{
  width: 100%;  
  height: 100%;  
  object-fit: fill; 
}
</style>
```
### 2、后端接收并保存图片
在后端项目文件夹创建static/images文件夹，用户上传的图片可以存储在此处。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717232042545-575743c8-e8d8-4591-b191-6e7ddeae5067.png#averageHue=%232e323a&clientId=u715f4784-a928-4&from=paste&height=229&id=u822e98f6&originHeight=343&originWidth=507&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=19269&status=done&style=none&taskId=u0d0a686c-4801-4658-9c3b-a9a416d097e&title=&width=338)
首先，在终端执行下面安装语句安装opencv-python:
```bash
pip install opencv-python -i https://pypi.tuna.tsinghua.edu.cn/simple
```
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717257800450-1d4cbb29-32ed-402d-83e0-b39018bd4133.png#averageHue=%23202329&clientId=u3c29d9ed-cfdb-4&from=paste&height=157&id=ub67e9f00&originHeight=235&originWidth=2180&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=67318&status=done&style=none&taskId=u39958350-029b-4a50-b880-3eeae3b1168&title=&width=1453.3333333333333)
需要编写后端接口接收uploadimages前端传过来的图像:
```vue
from flask import Flask, json, request, jsonify
from flask_cors import CORS
import pymysql
import cv2
import numpy as np
import os
DEBUG = True
app = Flask(__name__)
app.config.from_object(__name__)
CORS(app, resource={r'/*': {'origins': '*'}})

@app.route('/adduser', methods=['get', 'post'])
def adduser():
    username = request.form.get("username")
    password = request.form.get("password")
    print(username)
    print(password)
    return "已接收用户信息"

@app.route('/uploadimages', methods=['get', 'post'])
def uploadimages():
    username = request.form.get("username")
    img = request.files['file']
    picname=img.filename
    file = img.read()

    file = cv2.imdecode(np.frombuffer(file, np.uint8), cv2.IMREAD_COLOR)  # 解码为ndarray
    imgfile1_path = "./static/images/"+username+"/"
    if not os.path.exists(imgfile1_path):
        os.makedirs(imgfile1_path)
    img1_path = os.path.join(imgfile1_path, picname)
    cv2.imwrite(filename=img1_path, img=file)
    url = "http://127.0.0.1:5000/static/images/"+username+"/" + picname
    print(url)

    tempmap = {"url": url}
    return jsonify(tempmap)

    return "已接收用户图片信息"

if __name__ == '__main__':
    app.run(host="127.0.0.1", port=5000, debug=True)
```
在前端进行上传，发现能够传输到后端并且能进行存储，并返回图片链接。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717258232900-324fab18-002c-41cb-9a29-9b603d45ee0f.png#averageHue=%237dcce0&clientId=u3c29d9ed-cfdb-4&from=paste&height=391&id=uc1c3e25c&originHeight=587&originWidth=896&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=96658&status=done&style=none&taskId=uf4c5bd9d-1194-4473-9ce0-6e760063401&title=&width=597.3333333333334)
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717258190468-e49b5fc5-c046-4743-87a0-b9be61f9ced3.png#averageHue=%23303236&clientId=u3c29d9ed-cfdb-4&from=paste&height=236&id=u959a4b8c&originHeight=354&originWidth=507&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=19896&status=done&style=none&taskId=u615e0066-8be8-452a-97e9-5eae6e43e09&title=&width=338)
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717258250758-d024c03d-772f-4f51-acb8-effa3abb4927.png#averageHue=%231f2127&clientId=u3c29d9ed-cfdb-4&from=paste&height=95&id=u3d0cd44b&originHeight=142&originWidth=916&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=18574&status=done&style=none&taskId=u4de45c3f-3425-4e7b-bdce-de67a9d034f&title=&width=610.6666666666666)
访问链接可发现能够访问到上传的图像。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717258292100-38657a53-bb39-4eb2-a749-0881bf0d76b1.png#averageHue=%23a1a49e&clientId=u3c29d9ed-cfdb-4&from=paste&height=784&id=uff217c12&originHeight=1176&originWidth=1915&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=965249&status=done&style=none&taskId=u64ada352-d385-4620-9e2f-d353d401bd3&title=&width=1276.6666666666667)
### 3、数据库存储图片信息
存储图片信息可以为存Base64编码，但是比较吃资源，这里实现存储图片在本地，存储图片路径，用户通过路径访问服务器的图片从而实现存储功能。上一步骤已经生成了图像的链接，接下来把这部分存储到数据库当中。
在之前配置好的Phpstudy的PhpMyAdmin中创建数据库EditData。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717259427223-777feeaa-a05e-4c78-9b85-146a4fc01c49.png#averageHue=%23f5f4f4&clientId=u3a934c15-3b13-4&from=paste&height=675&id=uf788a6b0&originHeight=1013&originWidth=2550&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=274970&status=done&style=none&taskId=u2175a53b-83c3-4696-a9af-0d6a53407ba&title=&width=1700)
接着创建一个imgpath的数据表，并设计几个字段。
创建包含四个字段的imgpath数据表。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717259570996-44962257-874d-4f89-9ec9-e9da23088d79.png#averageHue=%23edecec&clientId=u3a934c15-3b13-4&from=paste&height=441&id=u8409e391&originHeight=662&originWidth=2554&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=199689&status=done&style=none&taskId=ua46b63cd-fd49-4311-8852-020d1fb11a0&title=&width=1702.6666666666667)
进行字段的定义，
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717259696437-b3a071f1-3a9b-4ee4-9e55-9a2205168fc7.png#averageHue=%23dfdede&clientId=u3a934c15-3b13-4&from=paste&height=883&id=u7c4901db&originHeight=1325&originWidth=2555&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=311873&status=done&style=none&taskId=u04e3f93e-654c-4e95-9a94-a5070d8ad25&title=&width=1703.3333333333333)
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717259931218-102a8197-b6a1-441b-ab03-0e69c0c375c3.png#averageHue=%23efedec&clientId=u3a934c15-3b13-4&from=paste&height=647&id=u970cb1c6&originHeight=970&originWidth=2549&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=291293&status=done&style=none&taskId=ubc0eb91a-1b8b-477c-9adf-506a19786cd&title=&width=1699.3333333333333)
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717259996808-509f3802-2d86-4d05-956e-deef3a56b606.png#averageHue=%23e9e8e8&clientId=u3a934c15-3b13-4&from=paste&height=282&id=u6a1d521f&originHeight=423&originWidth=2143&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=184091&status=done&style=none&taskId=u09917315-beed-4f2b-b880-7a99f26d651&title=&width=1428.6666666666667)
后端编写存储数据库的代码，完整的main.py代码如下:
```python
from flask import Flask, json, request, jsonify
from flask_cors import CORS
import pymysql
import cv2
import numpy as np
import os
DEBUG = True
app = Flask(__name__)
app.config.from_object(__name__)
CORS(app, resource={r'/*': {'origins': '*'}})

@app.route('/adduser', methods=['get', 'post'])
def adduser():
    username = request.form.get("username")
    password = request.form.get("password")
    print(username)
    print(password)
    return "已接收用户信息"

@app.route('/uploadimages', methods=['get', 'post'])
def uploadimages():
    username = request.form.get("username")
    img = request.files['file']
    picname=img.filename
    file = img.read()

    file = cv2.imdecode(np.frombuffer(file, np.uint8), cv2.IMREAD_COLOR)  # 解码为ndarray
    imgfile1_path = "./static/images/"+username+"/"
    if not os.path.exists(imgfile1_path):
        os.makedirs(imgfile1_path)
    img1_path = os.path.join(imgfile1_path, picname)
    cv2.imwrite(filename=img1_path, img=file)
    url = "http://127.0.0.1:5000/static/images/"+username+"/" + picname
    print(url)
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use editdata')
    sql = "INSERT INTO  `imgpath` (`username`,`url`,`picname`) VALUES('" + str(username) + "','" + str(url) + "','" + str(picname) + "');"
    ""
    print(sql)
    count = cursor.execute(sql)
    # print(count)
    conn.commit()
    cursor.close()
    conn.close()

    tempmap = {"url": url}
    return jsonify(tempmap)

    return "已接收用户图片信息"

if __name__ == '__main__':
    app.run(host="127.0.0.1", port=5000, debug=True)

```
前端上传图像，后端接收对应的数据，保存在本地后生成链接，存入地址信息至数据库。测试后发现，可以存储到数据库当中了。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717260451166-fd433409-6cd2-497d-918d-01752a616258.png#averageHue=%23f0f0eb&clientId=u3a934c15-3b13-4&from=paste&height=631&id=u04768062&originHeight=946&originWidth=2546&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=334067&status=done&style=none&taskId=udb254c13-564b-42ec-80b2-77149383664&title=&width=1697.3333333333333)
### 4、OCR项目在线体验
登录[Aistudio](https://aistudio.baidu.com/projectdetail/507159?channelType=0&channel=0)平台。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1716772939396-e4d37358-aab5-4b8a-89d6-86b44b8fdb7e.png#averageHue=%238da088&clientId=ue42b8057-fc1d-4&from=paste&height=984&id=uc3257921&originHeight=984&originWidth=1912&originalType=binary&ratio=1&rotation=0&showTitle=false&size=615881&status=done&style=none&taskId=u490ea612-90c2-481c-85d9-f05b7d2cb1f&title=&width=1912)
找到示例项目。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1716773086576-41d5bfbe-256f-4b59-972c-e690a093aeda.png#averageHue=%23eeebc8&clientId=ue42b8057-fc1d-4&from=paste&height=913&id=u75a17f3f&originHeight=913&originWidth=1905&originalType=binary&ratio=1&rotation=0&showTitle=false&size=311407&status=done&style=none&taskId=u1e1a7b8c-d53c-4995-87aa-8e7879a8af5&title=&width=1905)
可以根据项目的说明在线体验一下。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1716773176287-069a0dd5-78ec-41c6-a027-a938b1cb6c55.png#averageHue=%23d2b48c&clientId=ue42b8057-fc1d-4&from=paste&height=927&id=ube75d745&originHeight=927&originWidth=1907&originalType=binary&ratio=1&rotation=0&showTitle=false&size=227550&status=done&style=none&taskId=u121e796e-723d-45da-a93f-c719af6bd7f&title=&width=1907)

### 5、OCR项目本地部署
#### 5.1、PaddleOCR准备
除了之前准备的PaddlePaddle环境，还需要PaddleOCR环境。
PaddleOCR码云地址：[https://gitee.com/paddlepaddle/PaddleOCR](https://gitee.com/paddlepaddle/PaddleOCR)
模型地址:[https://github.com/PaddlePaddle/PaddleOCR/blob/static/doc/doc_ch/algorithm_overview.md](https://github.com/PaddlePaddle/PaddleOCR/blob/static/doc/doc_ch/algorithm_overview.md)
快速开始:[https://gitee.com/paddlepaddle/PaddleOCR/blob/main/doc/doc_ch/quickstart.md](https://gitee.com/paddlepaddle/PaddleOCR/blob/main/doc/doc_ch/quickstart.md)
先安装PaddleOCR whl包，执行如下指令:
```python
pip install "paddleocr>=2.0.1" -i https://pypi.tuna.tsinghua.edu.cn/simple --user  # 推荐使用2.0.1+版本
```
python终端执行:
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717262680204-60d08acd-6640-4fb5-9469-f5a5af5a89fb.png#averageHue=%2320242b&clientId=u3a934c15-3b13-4&from=paste&height=256&id=u66da408b&originHeight=384&originWidth=2167&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=128272&status=done&style=none&taskId=u5d1cfc8a-4437-49af-82f8-087f35d38ed&title=&width=1444.6666666666667)
安装完成后，上传一张需要识别的测试图片在test.py相同路径下，修改test.py代码进行测试。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717263044479-992b0a27-b5f0-4217-98b3-5719a4a17c7b.png#averageHue=%232e333b&clientId=u3a934c15-3b13-4&from=paste&height=205&id=ua8e63d54&originHeight=307&originWidth=513&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=18078&status=done&style=none&taskId=u55487c75-9ae9-41b9-8e94-dd65263db6f&title=&width=342)
```python
import paddle

print(paddle.__version__)
paddle.utils.run_check()

from paddleocr import PaddleOCR, draw_ocr

# Paddleocr目前支持的多语言语种可以通过修改lang参数进行切换
# 例如`ch`, `en`, `fr`, `german`, `korean`, `japan`
ocr = PaddleOCR(use_angle_cls=True, lang="ch")  # need to run only once to download and load model into memory
img_path = './test.png'
result = ocr.ocr(img_path, cls=True)
for idx in range(len(result)):
    res = result[idx]
    for line in res:
        print(line)

# 显示结果
from PIL import Image
result = result[0]
image = Image.open(img_path).convert('RGB')
boxes = [line[0] for line in result]
txts = [line[1][0] for line in result]
scores = [line[1][1] for line in result]
im_show = draw_ocr(image, boxes, txts, scores, font_path='./fonts/simfang.ttf')
im_show = Image.fromarray(im_show)
im_show.save('result.jpg')
```
运行后，可以看到出现了result.jpg,同时有运行结果输出。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717263139893-a98b82fc-a466-415c-87a3-f6c6e2d732b6.png#averageHue=%23222428&clientId=u3a934c15-3b13-4&from=paste&height=323&id=u76c774c2&originHeight=484&originWidth=2337&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=162382&status=done&style=none&taskId=uf1a47146-5c22-4925-9b9d-c0e774f4425&title=&width=1558)
result.jpg内容如下。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717263154697-a344fa7e-2abb-4fc5-a7f5-2a419a2d9eee.png#averageHue=%23b4b5b2&clientId=u3a934c15-3b13-4&from=paste&height=323&id=u04cd39c4&originHeight=485&originWidth=1795&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=730385&status=done&style=none&taskId=u1917a408-ebd4-45cd-b63f-809017fea9b&title=&width=1196.6666666666667)
至此，本地的环境配置完成，其他一些paddle模型本地运行也可以参考这种方式，安装对应的库，导入训练好的模型(或者自己重新训练也ok)，接着进行跑通即可在后续后端进行模型的使用。
#### 5.2、封装为api
加载模型其实比较费时，特别是加载一些比较大的模型时候，推理的时间会较少，因此，可以定义全局的模型，让flask运行时候就先加载好对应的模型，用的时候直接进行推理，能提高响应的速度，修改main.py代码如下。
```python
from flask import Flask, json, request, jsonify
from flask_cors import CORS
import pymysql
import cv2
import numpy as np
import os
import paddle
from paddleocr import PaddleOCR, draw_ocr


DEBUG = True
app = Flask(__name__)
app.config.from_object(__name__)
CORS(app, resource={r'/*': {'origins': '*'}})
ocr = PaddleOCR(use_angle_cls=True, lang="ch")  # need to run only once to download and load model into memory

@app.route('/adduser', methods=['get', 'post'])
def adduser():
    username = request.form.get("username")
    password = request.form.get("password")
    print(username)
    print(password)
    return "已接收用户信息"

@app.route('/uploadimages', methods=['get', 'post'])
def uploadimages():
    username = request.form.get("username")
    img = request.files['file']
    picname=img.filename
    file = img.read()

    file = cv2.imdecode(np.frombuffer(file, np.uint8), cv2.IMREAD_COLOR)  # 解码为ndarray
    imgfile1_path = "./static/images/"+username+"/"

    if not os.path.exists(imgfile1_path):
        os.makedirs(imgfile1_path)
    img1_path = os.path.join(imgfile1_path, picname)
    cv2.imwrite(filename=img1_path, img=file)

    img_path=imgfile1_path+picname
    result = ocr.ocr(img_path, cls=True)
    for idx in range(len(result)):
        res = result[idx]
        for line in res:
            print(line)
    url = "http://127.0.0.1:5000/static/images/"+username+"/" + picname
    print(url)
    conn = pymysql.connect(host='127.0.0.1', port=3306, user='root', password='root', charset='utf8')
    cursor = conn.cursor()
    conn.commit()
    cursor.execute('use editdata')
    sql = "INSERT INTO  `imgpath` (`username`,`url`,`picname`) VALUES('" + str(username) + "','" + str(url) + "','" + str(picname) + "');"
    ""
    print(sql)
    count = cursor.execute(sql)
    # print(count)
    conn.commit()
    cursor.close()
    conn.close()

    tempmap = {"url": url}
    return jsonify(tempmap)

    return "已接收用户图片信息"

if __name__ == '__main__':
    app.run(host="127.0.0.1", port=5000, debug=True)
```
前端上传需要识别的图片，传到后端后进行图像保存并识别文字，识别结果你可以根据自己的任务需求进行存数据库、传回前端等各种操作，至此，本地部署小模型的小模块实现完成了。
### 6、产线环境配置部署
如果本地资源不足(如无GPU算力，可以使用飞桨的模型产线功能)打开aistudio的**模型产线模块。**
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1716773676135-9d8fabee-cf8a-4c52-9671-2e3f4a844409.png#averageHue=%23e5eef4&clientId=ue42b8057-fc1d-4&from=paste&height=1000&id=ub7b03ff9&originHeight=1000&originWidth=1915&originalType=binary&ratio=1&rotation=0&showTitle=false&size=111667&status=done&style=none&taskId=uad00d781-712b-4521-8dcb-3ca26667b9b&title=&width=1915)
创建一个新的产线，选择OCR，设置好产线名称后确认创建：
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1716774013597-87a67651-8c04-476f-811d-81131c097d9e.png#averageHue=%2383a490&clientId=ue42b8057-fc1d-4&from=paste&height=1000&id=u75ff3ca6&originHeight=1000&originWidth=1917&originalType=binary&ratio=1&rotation=0&showTitle=false&size=157082&status=done&style=none&taskId=u091de574-9fc6-43a2-a4aa-582109c46eb&title=&width=1917)
可以选择数据集后进行训练后再部署，也可以直接进行部署。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1716774086738-b110d0e7-0ba9-49c3-8ea4-e156e21aead3.png#averageHue=%23fefefe&clientId=ue42b8057-fc1d-4&from=paste&height=934&id=uefd47955&originHeight=934&originWidth=1908&originalType=binary&ratio=1&rotation=0&showTitle=false&size=75650&status=done&style=none&taskId=u38fcd0d7-256e-45ea-803b-937818705c9&title=&width=1908)
如果选择直接部署，选择环境之后即可进行，因为需要使用CPU或GPU资源。需要A币进行开启，推荐大家开一个小会员体验一下，送1000个A币+100万Token。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717304546741-6b0b447c-8abe-40f7-b084-00c69e1b78e1.png#averageHue=%23fefefe&clientId=u1870715a-3d37-4&from=paste&height=900&id=uab625f7e&originHeight=1350&originWidth=2549&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=254328&status=done&style=none&taskId=ufbd37db0-1829-4fdd-bcb3-03053c56c81&title=&width=1699.3333333333333)
进行必须项的配置后点击开始部署。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717304758377-f93f7b38-b994-42e2-a3a7-915d32e6de17.png#averageHue=%23fefefe&clientId=u1870715a-3d37-4&from=paste&height=832&id=ue25bbf98&originHeight=1248&originWidth=1814&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=116709&status=done&style=none&taskId=u24f45bb1-268d-4990-b153-3608f74b9b8&title=&width=1209.3333333333333)
即可发现部署完成了，给出了使用的示例。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717304808860-7275b428-f2e8-472a-9ecf-ffeab4a6ea37.png#averageHue=%23afcda9&clientId=u1870715a-3d37-4&from=paste&height=887&id=ue0d1d2e3&originHeight=1331&originWidth=2538&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=247479&status=done&style=none&taskId=u739f8030-9508-47cf-8d64-a47152e6a8c&title=&width=1692)
在本地的test.py中编写代码测试一下,记得替换为自己的token：
```python
import base64
import pathlib
import pprint

import requests

API_URL = "https://105b32tccaj145nd.aistudio-hub.baidu.com/ocr"
# 请前往 https://aistudio.baidu.com/index/accessToken 查看 访问令牌 并替换
TOKEN = "替换为您的token"

# 设置鉴权信息
headers = {
    "Authorization": f"token {TOKEN}",
    "Content-Type": "application/json"
}

# 对本地图片进行Base64编码
image_path = "./test.png"
image_bytes = pathlib.Path(image_path).read_bytes()
image_base64 = base64.b64encode(image_bytes).decode('ascii')

# 设置请求体
payload = {
    "image": image_base64  # Base64编码的文件内容或者文件链接
}

# 调用
resp = requests.post(url=API_URL, json=payload, headers=headers)

# 处理接口返回数据
assert resp.status_code == 200
result = resp.json()["result"]
output_image_path = "output.jpg"
with open(output_image_path, "wb") as f:
    f.write(base64.b64decode(result["image"]))
print(f"OCR结果图保存在 {output_image_path}")
print("\n文本信息:")
pprint.pp(result["texts"])
```
运行后发现能够使用图像识别的功能，像本地部署一样封装为接口就可以前端调用使用了，可以让用户输入自己的接口，其他部分大家可以自行尝试。
![image.png](https://cdn.nlark.com/yuque/0/2024/png/44750262/1717304969386-7fdfa8e3-febb-49b1-9b28-0c1ba8195ec2.png#averageHue=%23232428&clientId=u1870715a-3d37-4&from=paste&height=1013&id=u43a6a6f6&originHeight=1519&originWidth=2541&originalType=binary&ratio=1.5&rotation=0&showTitle=false&size=334360&status=done&style=none&taskId=uf77a3fe7-5f81-46d9-9146-b18f4337aaf&title=&width=1694)
# 参考文章
[https://blog.csdn.net/m0_73995538/article/details/131216699](https://blog.csdn.net/m0_73995538/article/details/131216699)
[https://blog.csdn.net/m0_64338546/article/details/127149168](https://blog.csdn.net/m0_64338546/article/details/127149168)


