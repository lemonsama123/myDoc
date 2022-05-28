---
title: DQL
author: Lemon
top: false
cover: false
toc: true
mathjax: false
summary: 数据查询语言
tags:
  - 数据库
  - MySQL
categories:
  - MySQL
abbrlink: 54189da0
reprintPolicy: cc_by
date: 2022-01-27 15:21:36
coverImg:
img:
password:
---

## 一、概述

`Data Query Language`，简称 `DQL`，[数据查询语言](https://baike.baidu.com/item/DQL/4868445?fr=aladdin)，是用于查询数据的语言，是 `SQL` 的一个子集。

- 查询数据库数据，使用的最多的时 `select` 语句
- 有单表查询和多表查询以及嵌套查询
- 是数据库语言中最核心、重要的语句
- 使用频率最高的语句

用到的数据库代码：

```sql
/*
SQLyog Ultimate v10.00 Beta1
MySQL - 5.5.15 : Database - myemployees
*********************************************************************
*/


/*!40101 SET NAMES utf8 */;

/*!40101 SET SQL_MODE=''*/;

/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;
CREATE DATABASE /*!32312 IF NOT EXISTS*/`myemployees` /*!40100 DEFAULT CHARACTER SET gb2312 */;

USE `myemployees`;

/*Table structure for table `departments` */

DROP TABLE IF EXISTS `departments`;

CREATE TABLE `departments` (
  `department_id` int(4) NOT NULL AUTO_INCREMENT,
  `department_name` varchar(3) DEFAULT NULL,
  `manager_id` int(6) DEFAULT NULL,
  `location_id` int(4) DEFAULT NULL,
  PRIMARY KEY (`department_id`),
  KEY `loc_id_fk` (`location_id`),
  CONSTRAINT `loc_id_fk` FOREIGN KEY (`location_id`) REFERENCES `locations` (`location_id`)
) ENGINE=InnoDB AUTO_INCREMENT=271 DEFAULT CHARSET=gb2312;

/*Data for the table `departments` */

insert  into `departments`(`department_id`,`department_name`,`manager_id`,`location_id`) values (10,'Adm',200,1700),(20,'Mar',201,1800),(30,'Pur',114,1700),(40,'Hum',203,2400),(50,'Shi',121,1500),(60,'IT',103,1400),(70,'Pub',204,2700),(80,'Sal',145,2500),(90,'Exe',100,1700),(100,'Fin',108,1700),(110,'Acc',205,1700),(120,'Tre',NULL,1700),(130,'Cor',NULL,1700),(140,'Con',NULL,1700),(150,'Sha',NULL,1700),(160,'Ben',NULL,1700),(170,'Man',NULL,1700),(180,'Con',NULL,1700),(190,'Con',NULL,1700),(200,'Ope',NULL,1700),(210,'IT ',NULL,1700),(220,'NOC',NULL,1700),(230,'IT ',NULL,1700),(240,'Gov',NULL,1700),(250,'Ret',NULL,1700),(260,'Rec',NULL,1700),(270,'Pay',NULL,1700);

/*Table structure for table `employees` */

DROP TABLE IF EXISTS `employees`;

CREATE TABLE `employees` (
  `employee_id` int(6) NOT NULL AUTO_INCREMENT,
  `first_name` varchar(20) DEFAULT NULL,
  `last_name` varchar(25) DEFAULT NULL,
  `email` varchar(25) DEFAULT NULL,
  `phone_number` varchar(20) DEFAULT NULL,
  `job_id` varchar(10) DEFAULT NULL,
  `salary` double(10,2) DEFAULT NULL,
  `commission_pct` double(4,2) DEFAULT NULL,
  `manager_id` int(6) DEFAULT NULL,
  `department_id` int(4) DEFAULT NULL,
  `hiredate` datetime DEFAULT NULL,
  PRIMARY KEY (`employee_id`),
  KEY `dept_id_fk` (`department_id`),
  KEY `job_id_fk` (`job_id`),
  CONSTRAINT `dept_id_fk` FOREIGN KEY (`department_id`) REFERENCES `departments` (`department_id`),
  CONSTRAINT `job_id_fk` FOREIGN KEY (`job_id`) REFERENCES `jobs` (`job_id`)
) ENGINE=InnoDB AUTO_INCREMENT=207 DEFAULT CHARSET=gb2312;

/*Data for the table `employees` */

insert  into `employees`(`employee_id`,`first_name`,`last_name`,`email`,`phone_number`,`job_id`,`salary`,`commission_pct`,`manager_id`,`department_id`,`hiredate`) values (100,'Steven','K_ing','SKING','515.123.4567','AD_PRES',24000.00,NULL,NULL,90,'1992-04-03 00:00:00'),(101,'Neena','Kochhar','NKOCHHAR','515.123.4568','AD_VP',17000.00,NULL,100,90,'1992-04-03 00:00:00'),(102,'Lex','De Haan','LDEHAAN','515.123.4569','AD_VP',17000.00,NULL,100,90,'1992-04-03 00:00:00'),(103,'Alexander','Hunold','AHUNOLD','590.423.4567','IT_PROG',9000.00,NULL,102,60,'1992-04-03 00:00:00'),(104,'Bruce','Ernst','BERNST','590.423.4568','IT_PROG',6000.00,NULL,103,60,'1992-04-03 00:00:00'),(105,'David','Austin','DAUSTIN','590.423.4569','IT_PROG',4800.00,NULL,103,60,'1998-03-03 00:00:00'),(106,'Valli','Pataballa','VPATABAL','590.423.4560','IT_PROG',4800.00,NULL,103,60,'1998-03-03 00:00:00'),(107,'Diana','Lorentz','DLORENTZ','590.423.5567','IT_PROG',4200.00,NULL,103,60,'1998-03-03 00:00:00'),(108,'Nancy','Greenberg','NGREENBE','515.124.4569','FI_MGR',12000.00,NULL,101,100,'1998-03-03 00:00:00'),(109,'Daniel','Faviet','DFAVIET','515.124.4169','FI_ACCOUNT',9000.00,NULL,108,100,'1998-03-03 00:00:00'),(110,'John','Chen','JCHEN','515.124.4269','FI_ACCOUNT',8200.00,NULL,108,100,'2000-09-09 00:00:00'),(111,'Ismael','Sciarra','ISCIARRA','515.124.4369','FI_ACCOUNT',7700.00,NULL,108,100,'2000-09-09 00:00:00'),(112,'Jose Manuel','Urman','JMURMAN','515.124.4469','FI_ACCOUNT',7800.00,NULL,108,100,'2000-09-09 00:00:00'),(113,'Luis','Popp','LPOPP','515.124.4567','FI_ACCOUNT',6900.00,NULL,108,100,'2000-09-09 00:00:00'),(114,'Den','Raphaely','DRAPHEAL','515.127.4561','PU_MAN',11000.00,NULL,100,30,'2000-09-09 00:00:00'),(115,'Alexander','Khoo','AKHOO','515.127.4562','PU_CLERK',3100.00,NULL,114,30,'2000-09-09 00:00:00'),(116,'Shelli','Baida','SBAIDA','515.127.4563','PU_CLERK',2900.00,NULL,114,30,'2000-09-09 00:00:00'),(117,'Sigal','Tobias','STOBIAS','515.127.4564','PU_CLERK',2800.00,NULL,114,30,'2000-09-09 00:00:00'),(118,'Guy','Himuro','GHIMURO','515.127.4565','PU_CLERK',2600.00,NULL,114,30,'2000-09-09 00:00:00'),(119,'Karen','Colmenares','KCOLMENA','515.127.4566','PU_CLERK',2500.00,NULL,114,30,'2000-09-09 00:00:00'),(120,'Matthew','Weiss','MWEISS','650.123.1234','ST_MAN',8000.00,NULL,100,50,'2004-02-06 00:00:00'),(121,'Adam','Fripp','AFRIPP','650.123.2234','ST_MAN',8200.00,NULL,100,50,'2004-02-06 00:00:00'),(122,'Payam','Kaufling','PKAUFLIN','650.123.3234','ST_MAN',7900.00,NULL,100,50,'2004-02-06 00:00:00'),(123,'Shanta','Vollman','SVOLLMAN','650.123.4234','ST_MAN',6500.00,NULL,100,50,'2004-02-06 00:00:00'),(124,'Kevin','Mourgos','KMOURGOS','650.123.5234','ST_MAN',5800.00,NULL,100,50,'2004-02-06 00:00:00'),(125,'Julia','Nayer','JNAYER','650.124.1214','ST_CLERK',3200.00,NULL,120,50,'2004-02-06 00:00:00'),(126,'Irene','Mikkilineni','IMIKKILI','650.124.1224','ST_CLERK',2700.00,NULL,120,50,'2004-02-06 00:00:00'),(127,'James','Landry','JLANDRY','650.124.1334','ST_CLERK',2400.00,NULL,120,50,'2004-02-06 00:00:00'),(128,'Steven','Markle','SMARKLE','650.124.1434','ST_CLERK',2200.00,NULL,120,50,'2004-02-06 00:00:00'),(129,'Laura','Bissot','LBISSOT','650.124.5234','ST_CLERK',3300.00,NULL,121,50,'2004-02-06 00:00:00'),(130,'Mozhe','Atkinson','MATKINSO','650.124.6234','ST_CLERK',2800.00,NULL,121,50,'2004-02-06 00:00:00'),(131,'James','Marlow','JAMRLOW','650.124.7234','ST_CLERK',2500.00,NULL,121,50,'2004-02-06 00:00:00'),(132,'TJ','Olson','TJOLSON','650.124.8234','ST_CLERK',2100.00,NULL,121,50,'2004-02-06 00:00:00'),(133,'Jason','Mallin','JMALLIN','650.127.1934','ST_CLERK',3300.00,NULL,122,50,'2004-02-06 00:00:00'),(134,'Michael','Rogers','MROGERS','650.127.1834','ST_CLERK',2900.00,NULL,122,50,'2002-12-23 00:00:00'),(135,'Ki','Gee','KGEE','650.127.1734','ST_CLERK',2400.00,NULL,122,50,'2002-12-23 00:00:00'),(136,'Hazel','Philtanker','HPHILTAN','650.127.1634','ST_CLERK',2200.00,NULL,122,50,'2002-12-23 00:00:00'),(137,'Renske','Ladwig','RLADWIG','650.121.1234','ST_CLERK',3600.00,NULL,123,50,'2002-12-23 00:00:00'),(138,'Stephen','Stiles','SSTILES','650.121.2034','ST_CLERK',3200.00,NULL,123,50,'2002-12-23 00:00:00'),(139,'John','Seo','JSEO','650.121.2019','ST_CLERK',2700.00,NULL,123,50,'2002-12-23 00:00:00'),(140,'Joshua','Patel','JPATEL','650.121.1834','ST_CLERK',2500.00,NULL,123,50,'2002-12-23 00:00:00'),(141,'Trenna','Rajs','TRAJS','650.121.8009','ST_CLERK',3500.00,NULL,124,50,'2002-12-23 00:00:00'),(142,'Curtis','Davies','CDAVIES','650.121.2994','ST_CLERK',3100.00,NULL,124,50,'2002-12-23 00:00:00'),(143,'Randall','Matos','RMATOS','650.121.2874','ST_CLERK',2600.00,NULL,124,50,'2002-12-23 00:00:00'),(144,'Peter','Vargas','PVARGAS','650.121.2004','ST_CLERK',2500.00,NULL,124,50,'2002-12-23 00:00:00'),(145,'John','Russell','JRUSSEL','011.44.1344.429268','SA_MAN',14000.00,0.40,100,80,'2002-12-23 00:00:00'),(146,'Karen','Partners','KPARTNER','011.44.1344.467268','SA_MAN',13500.00,0.30,100,80,'2002-12-23 00:00:00'),(147,'Alberto','Errazuriz','AERRAZUR','011.44.1344.429278','SA_MAN',12000.00,0.30,100,80,'2002-12-23 00:00:00'),(148,'Gerald','Cambrault','GCAMBRAU','011.44.1344.619268','SA_MAN',11000.00,0.30,100,80,'2002-12-23 00:00:00'),(149,'Eleni','Zlotkey','EZLOTKEY','011.44.1344.429018','SA_MAN',10500.00,0.20,100,80,'2002-12-23 00:00:00'),(150,'Peter','Tucker','PTUCKER','011.44.1344.129268','SA_REP',10000.00,0.30,145,80,'2014-03-05 00:00:00'),(151,'David','Bernstein','DBERNSTE','011.44.1344.345268','SA_REP',9500.00,0.25,145,80,'2014-03-05 00:00:00'),(152,'Peter','Hall','PHALL','011.44.1344.478968','SA_REP',9000.00,0.25,145,80,'2014-03-05 00:00:00'),(153,'Christopher','Olsen','COLSEN','011.44.1344.498718','SA_REP',8000.00,0.20,145,80,'2014-03-05 00:00:00'),(154,'Nanette','Cambrault','NCAMBRAU','011.44.1344.987668','SA_REP',7500.00,0.20,145,80,'2014-03-05 00:00:00'),(155,'Oliver','Tuvault','OTUVAULT','011.44.1344.486508','SA_REP',7000.00,0.15,145,80,'2014-03-05 00:00:00'),(156,'Janette','K_ing','JKING','011.44.1345.429268','SA_REP',10000.00,0.35,146,80,'2014-03-05 00:00:00'),(157,'Patrick','Sully','PSULLY','011.44.1345.929268','SA_REP',9500.00,0.35,146,80,'2014-03-05 00:00:00'),(158,'Allan','McEwen','AMCEWEN','011.44.1345.829268','SA_REP',9000.00,0.35,146,80,'2014-03-05 00:00:00'),(159,'Lindsey','Smith','LSMITH','011.44.1345.729268','SA_REP',8000.00,0.30,146,80,'2014-03-05 00:00:00'),(160,'Louise','Doran','LDORAN','011.44.1345.629268','SA_REP',7500.00,0.30,146,80,'2014-03-05 00:00:00'),(161,'Sarath','Sewall','SSEWALL','011.44.1345.529268','SA_REP',7000.00,0.25,146,80,'2014-03-05 00:00:00'),(162,'Clara','Vishney','CVISHNEY','011.44.1346.129268','SA_REP',10500.00,0.25,147,80,'2014-03-05 00:00:00'),(163,'Danielle','Greene','DGREENE','011.44.1346.229268','SA_REP',9500.00,0.15,147,80,'2014-03-05 00:00:00'),(164,'Mattea','Marvins','MMARVINS','011.44.1346.329268','SA_REP',7200.00,0.10,147,80,'2014-03-05 00:00:00'),(165,'David','Lee','DLEE','011.44.1346.529268','SA_REP',6800.00,0.10,147,80,'2014-03-05 00:00:00'),(166,'Sundar','Ande','SANDE','011.44.1346.629268','SA_REP',6400.00,0.10,147,80,'2014-03-05 00:00:00'),(167,'Amit','Banda','ABANDA','011.44.1346.729268','SA_REP',6200.00,0.10,147,80,'2014-03-05 00:00:00'),(168,'Lisa','Ozer','LOZER','011.44.1343.929268','SA_REP',11500.00,0.25,148,80,'2014-03-05 00:00:00'),(169,'Harrison','Bloom','HBLOOM','011.44.1343.829268','SA_REP',10000.00,0.20,148,80,'2014-03-05 00:00:00'),(170,'Tayler','Fox','TFOX','011.44.1343.729268','SA_REP',9600.00,0.20,148,80,'2014-03-05 00:00:00'),(171,'William','Smith','WSMITH','011.44.1343.629268','SA_REP',7400.00,0.15,148,80,'2014-03-05 00:00:00'),(172,'Elizabeth','Bates','EBATES','011.44.1343.529268','SA_REP',7300.00,0.15,148,80,'2014-03-05 00:00:00'),(173,'Sundita','Kumar','SKUMAR','011.44.1343.329268','SA_REP',6100.00,0.10,148,80,'2014-03-05 00:00:00'),(174,'Ellen','Abel','EABEL','011.44.1644.429267','SA_REP',11000.00,0.30,149,80,'2014-03-05 00:00:00'),(175,'Alyssa','Hutton','AHUTTON','011.44.1644.429266','SA_REP',8800.00,0.25,149,80,'2014-03-05 00:00:00'),(176,'Jonathon','Taylor','JTAYLOR','011.44.1644.429265','SA_REP',8600.00,0.20,149,80,'2014-03-05 00:00:00'),(177,'Jack','Livingston','JLIVINGS','011.44.1644.429264','SA_REP',8400.00,0.20,149,80,'2014-03-05 00:00:00'),(178,'Kimberely','Grant','KGRANT','011.44.1644.429263','SA_REP',7000.00,0.15,149,NULL,'2014-03-05 00:00:00'),(179,'Charles','Johnson','CJOHNSON','011.44.1644.429262','SA_REP',6200.00,0.10,149,80,'2014-03-05 00:00:00'),(180,'Winston','Taylor','WTAYLOR','650.507.9876','SH_CLERK',3200.00,NULL,120,50,'2014-03-05 00:00:00'),(181,'Jean','Fleaur','JFLEAUR','650.507.9877','SH_CLERK',3100.00,NULL,120,50,'2014-03-05 00:00:00'),(182,'Martha','Sullivan','MSULLIVA','650.507.9878','SH_CLERK',2500.00,NULL,120,50,'2014-03-05 00:00:00'),(183,'Girard','Geoni','GGEONI','650.507.9879','SH_CLERK',2800.00,NULL,120,50,'2014-03-05 00:00:00'),(184,'Nandita','Sarchand','NSARCHAN','650.509.1876','SH_CLERK',4200.00,NULL,121,50,'2014-03-05 00:00:00'),(185,'Alexis','Bull','ABULL','650.509.2876','SH_CLERK',4100.00,NULL,121,50,'2014-03-05 00:00:00'),(186,'Julia','Dellinger','JDELLING','650.509.3876','SH_CLERK',3400.00,NULL,121,50,'2014-03-05 00:00:00'),(187,'Anthony','Cabrio','ACABRIO','650.509.4876','SH_CLERK',3000.00,NULL,121,50,'2014-03-05 00:00:00'),(188,'Kelly','Chung','KCHUNG','650.505.1876','SH_CLERK',3800.00,NULL,122,50,'2014-03-05 00:00:00'),(189,'Jennifer','Dilly','JDILLY','650.505.2876','SH_CLERK',3600.00,NULL,122,50,'2014-03-05 00:00:00'),(190,'Timothy','Gates','TGATES','650.505.3876','SH_CLERK',2900.00,NULL,122,50,'2014-03-05 00:00:00'),(191,'Randall','Perkins','RPERKINS','650.505.4876','SH_CLERK',2500.00,NULL,122,50,'2014-03-05 00:00:00'),(192,'Sarah','Bell','SBELL','650.501.1876','SH_CLERK',4000.00,NULL,123,50,'2014-03-05 00:00:00'),(193,'Britney','Everett','BEVERETT','650.501.2876','SH_CLERK',3900.00,NULL,123,50,'2014-03-05 00:00:00'),(194,'Samuel','McCain','SMCCAIN','650.501.3876','SH_CLERK',3200.00,NULL,123,50,'2014-03-05 00:00:00'),(195,'Vance','Jones','VJONES','650.501.4876','SH_CLERK',2800.00,NULL,123,50,'2014-03-05 00:00:00'),(196,'Alana','Walsh','AWALSH','650.507.9811','SH_CLERK',3100.00,NULL,124,50,'2014-03-05 00:00:00'),(197,'Kevin','Feeney','KFEENEY','650.507.9822','SH_CLERK',3000.00,NULL,124,50,'2014-03-05 00:00:00'),(198,'Donald','OConnell','DOCONNEL','650.507.9833','SH_CLERK',2600.00,NULL,124,50,'2014-03-05 00:00:00'),(199,'Douglas','Grant','DGRANT','650.507.9844','SH_CLERK',2600.00,NULL,124,50,'2014-03-05 00:00:00'),(200,'Jennifer','Whalen','JWHALEN','515.123.4444','AD_ASST',4400.00,NULL,101,10,'2016-03-03 00:00:00'),(201,'Michael','Hartstein','MHARTSTE','515.123.5555','MK_MAN',13000.00,NULL,100,20,'2016-03-03 00:00:00'),(202,'Pat','Fay','PFAY','603.123.6666','MK_REP',6000.00,NULL,201,20,'2016-03-03 00:00:00'),(203,'Susan','Mavris','SMAVRIS','515.123.7777','HR_REP',6500.00,NULL,101,40,'2016-03-03 00:00:00'),(204,'Hermann','Baer','HBAER','515.123.8888','PR_REP',10000.00,NULL,101,70,'2016-03-03 00:00:00'),(205,'Shelley','Higgins','SHIGGINS','515.123.8080','AC_MGR',12000.00,NULL,101,110,'2016-03-03 00:00:00'),(206,'William','Gietz','WGIETZ','515.123.8181','AC_ACCOUNT',8300.00,NULL,205,110,'2016-03-03 00:00:00');

/*Table structure for table `jobs` */

DROP TABLE IF EXISTS `jobs`;

CREATE TABLE `jobs` (
  `job_id` varchar(10) NOT NULL,
  `job_title` varchar(35) DEFAULT NULL,
  `min_salary` int(6) DEFAULT NULL,
  `max_salary` int(6) DEFAULT NULL,
  PRIMARY KEY (`job_id`)
) ENGINE=InnoDB DEFAULT CHARSET=gb2312;

/*Data for the table `jobs` */

insert  into `jobs`(`job_id`,`job_title`,`min_salary`,`max_salary`) values ('AC_ACCOUNT','Public Accountant',4200,9000),('AC_MGR','Accounting Manager',8200,16000),('AD_ASST','Administration Assistant',3000,6000),('AD_PRES','President',20000,40000),('AD_VP','Administration Vice President',15000,30000),('FI_ACCOUNT','Accountant',4200,9000),('FI_MGR','Finance Manager',8200,16000),('HR_REP','Human Resources Representative',4000,9000),('IT_PROG','Programmer',4000,10000),('MK_MAN','Marketing Manager',9000,15000),('MK_REP','Marketing Representative',4000,9000),('PR_REP','Public Relations Representative',4500,10500),('PU_CLERK','Purchasing Clerk',2500,5500),('PU_MAN','Purchasing Manager',8000,15000),('SA_MAN','Sales Manager',10000,20000),('SA_REP','Sales Representative',6000,12000),('SH_CLERK','Shipping Clerk',2500,5500),('ST_CLERK','Stock Clerk',2000,5000),('ST_MAN','Stock Manager',5500,8500);

/*Table structure for table `locations` */

DROP TABLE IF EXISTS `locations`;

CREATE TABLE `locations` (
  `location_id` int(11) NOT NULL AUTO_INCREMENT,
  `street_address` varchar(40) DEFAULT NULL,
  `postal_code` varchar(12) DEFAULT NULL,
  `city` varchar(30) DEFAULT NULL,
  `state_province` varchar(25) DEFAULT NULL,
  `country_id` varchar(2) DEFAULT NULL,
  PRIMARY KEY (`location_id`)
) ENGINE=InnoDB AUTO_INCREMENT=3201 DEFAULT CHARSET=gb2312;

/*Data for the table `locations` */

insert  into `locations`(`location_id`,`street_address`,`postal_code`,`city`,`state_province`,`country_id`) values (1000,'1297 Via Cola di Rie','00989','Roma',NULL,'IT'),(1100,'93091 Calle della Testa','10934','Venice',NULL,'IT'),(1200,'2017 Shinjuku-ku','1689','Tokyo','Tokyo Prefecture','JP'),(1300,'9450 Kamiya-cho','6823','Hiroshima',NULL,'JP'),(1400,'2014 Jabberwocky Rd','26192','Southlake','Texas','US'),(1500,'2011 Interiors Blvd','99236','South San Francisco','California','US'),(1600,'2007 Zagora St','50090','South Brunswick','New Jersey','US'),(1700,'2004 Charade Rd','98199','Seattle','Washington','US'),(1800,'147 Spadina Ave','M5V 2L7','Toronto','Ontario','CA'),(1900,'6092 Boxwood St','YSW 9T2','Whitehorse','Yukon','CA'),(2000,'40-5-12 Laogianggen','190518','Beijing',NULL,'CN'),(2100,'1298 Vileparle (E)','490231','Bombay','Maharashtra','IN'),(2200,'12-98 Victoria Street','2901','Sydney','New South Wales','AU'),(2300,'198 Clementi North','540198','Singapore',NULL,'SG'),(2400,'8204 Arthur St',NULL,'London',NULL,'UK'),(2500,'Magdalen Centre, The Oxford Science Park','OX9 9ZB','Oxford','Oxford','UK'),(2600,'9702 Chester Road','09629850293','Stretford','Manchester','UK'),(2700,'Schwanthalerstr. 7031','80925','Munich','Bavaria','DE'),(2800,'Rua Frei Caneca 1360 ','01307-002','Sao Paulo','Sao Paulo','BR'),(2900,'20 Rue des Corps-Saints','1730','Geneva','Geneve','CH'),(3000,'Murtenstrasse 921','3095','Bern','BE','CH'),(3100,'Pieter Breughelstraat 837','3029SK','Utrecht','Utrecht','NL'),(3200,'Mariano Escobedo 9991','11932','Mexico City','Distrito Federal,','MX');

/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;
```



## 二、语法

```mysql
SELECT [ALL|DISTINCT]
{*|table.*|table.fidld1[as alias1][,table.filed2[as alias2]][,...]}
FROM tableName [as table_alias] #联合查询
[WHERE ...] #筛选条件
[GROUP BY ...] #指定结果按哪几个字段分组
[HAVING] #过滤分组的记录必须满足的次要条件
[ORDER BY] #指定查询记录按一个或多个字段排序
[LIMIT {[offset,]row_count|row_countOFFSET offset}]; #指定查询的距离从哪条至哪条
```

> `[]` 表示可选，`{}` 表示必有一个被选。

## 三、查询指定表的字段

### 3.1 语法

```mysql
as 别名];
```

> `AS` 为起别名

- 可给数据列取别名
- 可给表取别名
- 可把经计算或直接的结果用一个新名称来代替
- `AS` 关键字可以省略

示例 1：

```mysql
SELECT
	`last_name`,
	`salary`,
	`email`
FROM
	`employees`;
```

![image-20220127190826297](https://s2.loli.net/2022/01/27/RANZlFin8YrJxyE.png)

示例 2：

```sql
SELECT
	`last_name` AS 姓,
	`salary` AS 工资,
	`email` AS 邮箱
FROM
	`employees`;
```

![image-20220127190916417](https://s2.loli.net/2022/01/27/bGLmVNEvQayq8sZ.png)

> 通过上面两个示例我们也看到了使用别名和不使用别名的区别。

同时我们可以通过 `SELECT * FROM table_name` 来查询所有字段。

### 3.2 关键字 `DISTINCT 和 ALL`

作用：去重，即如果在查询结果中有重复的记录，只返回一条。

```mysql
SELECT DISTINCT `department_id` FROM `employees`;
```

这条语句查询结果为：

![image-20220127185804019](https://s2.loli.net/2022/01/27/rBRvxU3VlwSIXJD.png)

如果什么也不写，则默认为 `ALL`，即 `SELECT ALL * FROM table_name;` 和 `SELECT * FROM table_name` 是等价的。

> 我们可以通过 `SELECT DISTINCT COUNT(字段名) FROM table_name` 来查询某个字段有多少不的值。

### 3.3 常量、表达式与函数

- 查询常量：`SELECT 常量;`
- 查询表达式：`SELECT 表达式;`
- 查询函数：`SELECT 函数名(参数列表);`

例如：

```mysql
SELECT 100;
```

![image-20220127191836720](https://s2.loli.net/2022/01/27/IYoBAeQwZW3jPVG.png)

```mysql
SELECT 100*99;
```

![image-20220127191905109](https://s2.loli.net/2022/01/27/4fd7eiZ8W1YTUqc.png)

```mysql
SELECT VERSION();
```

![image-20220127191951436](https://s2.loli.net/2022/01/27/YrPOJLpQI8dDEHy.png)

#### 3.3.1 常用函数介绍

##### `concat()` 函数

功能：拼接字符（串）

语法：`SELECT CONCAT(字符1，字符2，字符3...);`

##### `ifnull()` 函数

功能：判断某字段或表达式是否为 `null`，如果为 `null` 返回指定的值，否则返回原本的值

语法：`SELECT ifnull(字段,字段为null是返回的值);`

##### `isnull()` 函数

功能：判断某字段或表达式是否为 `null`，如果是，则返回 1，否则返回 0.

语法：`SELECT ISNULL(字段) FROM 表名;`

##### 例子

例一：

```mysql
#案例：查询员工名和姓连接成一个字段，并显示为 姓名
SELECT CONCAT(last_name,first_name) AS 姓名 FROM employees;
```

![img](https://s2.loli.net/2022/01/27/TMXFPfCl1qQuetw.png)

例二：

```mysql
SELECT 
	IFNULL(commission_pct,0) AS 奖金率,
	commission_pct
FROM 
	employees;
```

![img](https://s2.loli.net/2022/01/27/R4qmEDSbFGakt6h.png)

例三：

```mysql
SELECT ISNULL(commission_pct),commission_pct FROM employees;
```

![img](https://s2.loli.net/2022/01/27/xAHkQopN48zgq7c.png)

## 四、条件查询

作用：用于过滤、筛选出表中符合**筛选条件**的记录。

筛选条件可由一个或多个逻辑表达式组成，结果一般为真或假。

条件运算符有：`> < = <> != >= <= <=>`.

> `<>` 同 `!=` 表示不等于，`<=>` 是安全对于。

逻辑运算符有：

| 操作符名称    | 语法                                                         | 描述                       |
| ------------- | ------------------------------------------------------------ | -------------------------- |
| `AND` 或 `&&` | `条件表达式1 AND 条件表达式2` 或 `条件表达式1 && 条件表达式2` | 逻辑与，全真则真，一假则假 |
| `OR` 或 `||`  | `条件表达式1 OR 条件表达式2` 或 `条件表达式1 || 条件表达式2` | 逻辑或，一真则真，全假则假 |
| `NOT` 或 `!`  | `NOT 条件表达式` 或 `!条件表达式`                            | 逻辑假，真则假，假则真     |

除了按条件表达式查询外，还有模糊查询，模糊查询用到的关键字有：

- `LIKE`：一般搭配通配符使用，可以匹配字符型或数值型。
- `BETWEEN ... AND ...`.
- `IN`.
- `IS NULL|IS NOT NULL`：用于判断 `NULL` 值。

### 4.1 按条件表达式或逻辑表达式查询

> 逻辑表达式是多个通过逻辑运算符连接起来的条件表达式。

语法：

```mysql
SELECT 
	字段1 [[AS] 别名1],
	字段2 [[AS] 别名2],
	字段3 [[AS] 别名3],
	...
	字段n [[AS] 别名n]
WHERE
	条件表达式1 [逻辑运算符1 条件表达式2 [逻辑运算符1 条件表达式2...]];
```

### 4.2 按条件表达式或逻辑表达式查询的例子

例一：

```mysql
#查询工资大于 12000 的员工信息
SELECT * FROM employees WHERE salary > 12000;
```

![image-20220127225520178](https://s2.loli.net/2022/01/27/b52jitMvfFBZSeu.png)

例二：

```mysql
#查询部门编号不等于90号的员工们和部门编号
SELECT last_name,department_id FROM employees WHERE department_id <> 90;
```

![image-20220127225647042](https://s2.loli.net/2022/01/27/sGWpYuDeX6oyOJN.png)

例三：

```mysql
SELECT
	last_name AS 名,
	salary AS 工资,
	salary*12*IFNULL(commission_pct,0)
FROM
	employees
WHERE
	salary>=10000 AND salary<=20000;
```

![image-20220127225854682](https://s2.loli.net/2022/01/27/MVS1h2HFQGvn9wT.png)

例四：

```mysql
#查询部门编号不是在90到110之间，或者工资高于15000的通过信息
SELECT
	*
FROM
	employees
WHERE
	NOT(department_id>=90 AND department_id<= 110) OR salary>15000;
```

![image-20220127230028325](https://s2.loli.net/2022/01/27/lugb7aPN4QcCLYM.png)

### 4.3 模糊查询

| 操作符名称                | 语法                      | 描述                                             |
| ------------------------- | ------------------------- | ------------------------------------------------ |
| `IS NULL`                 | `a is NULL`               | 若 a 为 `NULL`，则结果为真                       |
| `IS NOT NULL`             | `a IS NOT BULL`           | 若 a 不为 `NULL`，则结果为真                     |
| `BETWEEN ... AND ...`     | `a BETWEEN b AND c `      | 若 a 范围在 b 和 c 之间，则结果为真              |
| `NOT BETWEEN ... AND ...` | `a NOT  BETWEEN b AND c ` | 若 a 范围不在 b 和 c 之间，则结果为真            |
| `LIKE`                    | `a LIKE b`                | `SQL` 匹配模式，若 a 匹配 b，则结果为真          |
| `IN`                      | `a IN(a1,a2,a3,...)`      | 若 a 等于 a1、a2、a3......中的某一个，则结果为真 |

> 最常用的通配符有：`%` 和 `_`，分别表示任意多个字符（包括 0 个）和单个字符。

### 4.4 按条件查询的例子

例一：

```mysql
#查询员工名中包含字符 a 的员工信息
SELECT
	*
FROM 
	employees
WHERE
	last_name LIKE '%a%';
```

![image-20220127231151924](https://s2.loli.net/2022/01/27/tG1HaXxfW7q8h63.png)

例二：

```mysql
#查询员工名中第三个字符为 n，第五个字符为 l 的员工名和工资
SELECT 
	last_name,
	salary
FROM 
	employees
WHERE
	last_name LIKE '__n_l%';
```

![image-20220127231251874](https://s2.loli.net/2022/01/27/wKXGnmlIF9bEdYc.png)

例三：

```mysq
#查询员工名中第二个字符为 _ 的员工名
SELECT
	last_name
FROM
	employees
WHERE
	last_name LIKE '_$_%' ESCAPE '$';
```

![image-20220127231339095](https://s2.loli.net/2022/01/27/AIR8wuDdngWvMzH.png)

例四：

```mysql
#查询员工编号在100到120之间所有的员工信息
SELECT
	*
FROM
	employees
WHERE
	employee_id BETWEEN 100 AND 120;
```

![image-20220127231504799](https://s2.loli.net/2022/01/27/9B7uSOh4mwzeCqd.png)

例五：

```mysql
#查询员工的工种编号是 IT_PROG、AD_VP、AD_PRES 中的一个的员工名和工种编号
SELECT
	last_name,
	job_id
FROM 
	employees
WHERE
	job_id IN('IT_PROG','AD_VP','AD_PRES');
```

![image-20220127231609324](https://s2.loli.net/2022/01/27/JARVZEKrINedguo.png)

例六：

```mysql
#查询有奖金的员工名和奖金率
SELECT
	last_name,
	commission_pct
FROM 
	employees
WHERE
	commission_pct IS NOT NULL;
```

![image-20220127231719052](https://s2.loli.net/2022/01/27/zjqrQdApv2Omktg.png)

### 4.5 几点说明

1. `a BETWEEN b AND c` 等价于 `a >= b && a <= c `，故 b 和 c 的位置不可对调。
2. `BETWEEN ... AND ...` 包含临界值。
3. `=` 和 `<>` 不可以判断 `NULL`  值，`IS NULL` 或 `IS NOT NULL` 可以。
4. `IS NULL` 与 `<=>`比较

|           | 普通类型的数值 | `null`值 | 可读性 |
| --------- | -------------- | -------- | ------ |
| `IS NULL` | ×              | √        | √      |
| `<=>`     | √              | √        | ×      |

## 五、排序查询

语法：

```mysql
SELECT 查询列表 FROM 表 ORDER BY 查询列表 [ASC|
DESC]
```

> 1. `ASC` 代表升序，`DESC` 代表降序，不写默认为升序
> 2. `ORDER BY` 字句中支持单个字段、多个字段、表达式、函数、别名
> 3. `ORDER BY` 子句一般放在查询语句最后面，除 `LIMLT` 子句之外

### 5.1 例子

例一：

```mysql
#查询员工信息，要求工资从高到低排序
SELECT
	*
FROM
	`employees`
ORDER BY
	`salary` DESC;
```

![image-20220128125247588](https://s2.loli.net/2022/01/28/k5hpvGAN6xPgR7b.png)

例二：

```mysql
#查询部门编号>=90的员工信息，要求按入职时间的先后进行排序
SELECT
	*
FROM 
	`employees`
WHERE
	`department_id`>=90
ORDER BY
	hiredate ASC;
```

![image-20220128125901249](https://s2.loli.net/2022/01/28/Equ6NUDWtrwlkTj.png)

例三：

```mysql
#按年薪高低显示员工信息和年薪
SELECT
	*,
	salary*12*(IFNULL(commission_pct,0)+1) AS 年薪
FROM
	employees
ORDER BY
	年薪 DESC;
```

![image-20220128125936347](https://s2.loli.net/2022/01/28/ZgMeJKcfVxrRq47.png)

例四：

```mysql
#按姓名长度显示员工的姓名和工资
SELECT
	last_name AS 姓名,
	salary AS 工资
FROM
	employees
ORDER BY
	LENGTH(last_name) DESC;
```

![image-20220128130016993](https://s2.loli.net/2022/01/28/tL7bIBNC3o2F16E.png)

例五：

```mysql
#查询员工信息，要求先按工资升序排序，再按员工降序编号排序
SELECT
	*
FROM
	employees
ORDER BY
	salary ASC,
	employee_id DESC;
```

![](https://s3.bmp.ovh/imgs/2022/01/45b08060196f29a7.png)

## 六、分组查询

语法：

```mysql
SELECT 分组函数,分组后的字段
FROM 表
[WHERE 筛选条件]
GROUP BY 分组的字段
[HAVING 分组后的筛选]
[ORDER BY 排序列表
```

关于函数的详细介绍请参阅：[MySQL中的函数](/posts/1e2619a3.html)

分组查询中的筛选条件可分为两类：

|            | 数据源         | 位置                  | 关键字   |
| ---------- | -------------- | --------------------- | -------- |
| 分组前筛选 | 原始表         | `GROUP BY` 子句的前面 | `WHERE`  |
| 分组后筛选 | 分组后的结果集 | `GROUP BY` 子句的后面 | `HAVING` |

1. 分组函数做条件肯定是放在 `HAING` 子句中
2. 能用分组前筛选的，优先考虑使用分组前筛选
3. `GROUP BY` 子句支持单个字段分组，多个字段分组（多个 字段之间有用逗号隔开，没有顺序要求）、表达式或函数（用得较少）
4. 也可以添加排序（排序放在整个分组查询的最后）

### 6.1 例子

