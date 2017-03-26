   �����һƪ Springboot �����ĵ��������߽�׼��дд Springboot ������ʵ����һ�����ܽ���һЩ Springboot ��أ�һ����ʹ�ҽ������� Springboot ��ܡ�
   ����ҵ�绥�������е����ݲ������� Mybatis����������� Springboot ������� Mybatis �����û��ʹ�� Mybatis Annotation ���֣���ʹ�� xml ���� SQL����Ϊ�Ҿ��� SQL ��ҵ�����Ӧ�ø��룬����� DBA У�� SQL������ XML �Խϳ��� SQL �Ƚ�������
#### һ������ springboot-mybatis ����
it clone ���ع��� springboot-learning-example ����Ŀ��ַ�� GitHub �����濪ʼ���й��̲��裨Quick Start����
1. ���ݿ�׼��
a.�������ݿ� springbootdb��
```sql
CREATE DATABASE springbootdb;
```
b.������ city ��(��Ϊ��ϲ��ͽ��)
````sql
DROP TABLE IF EXISTS  `city`;
CREATE TABLE `city` (
  `id` int(10) unsigned NOT NULL AUTO_INCREMENT COMMENT '���б��',
  `province_id` int(10) unsigned  NOT NULL COMMENT 'ʡ�ݱ��',
  `city_name` varchar(25) DEFAULT NULL COMMENT '��������',
  `description` varchar(25) DEFAULT NULL COMMENT '����',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8;
````
c.��������
```sql
INSERT city VALUES (1 ,1,'������','BYSocket �ļ������롣');
```
2.��Ŀ�ṹ����
��Ŀ�ṹ����ͼ��ʾ��
![](pictures/76ec0560266f4997bb2f31fe3e678833.png)
org.spring.springboot.controller �C Controller ��

org.spring.springboot.dao �C ���ݲ����� DAO

org.spring.springboot.domain �C ʵ����

org.spring.springboot.service �C ҵ���߼���

Application �C Ӧ��������

application.properties �C Ӧ�������ļ���Ӧ���������Զ���ȡ����

3.�����ݿ�����

�� application.properties �ļ��� �޸���Ӧ������Դ���ã���������Դ��ַ���˺š�����ȡ������������ MySQL����������������� pom��Ȼ���޸����������á���

4.���빤��

����Ŀ��Ŀ¼ springboot-learning-example������ maven ָ�
```
mvn clean install
```
5.���й���

�Ҽ����� Application Ӧ��������� main ������Ȼ������������ʣ�
```
http://localhost:8080/api/city?cityName=������
```
���Կ������ص� JSON �����
```
{
    "id": 1,
    "provinceId": 1,
    "cityName": "������",
    "description": "�ҵļ������롣"
}
```
