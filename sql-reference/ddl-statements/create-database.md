# CREATE DATABASE {#create-database}

Creates a database. The use of`DATABASE`and`SCHEMA`is interchangeable. They mean the same thing.

创建一个数据库。

改变表或者分区表的存储位置

## Synopsis\(文法\) {#synopsis}

```
CREATE (DATABASE|SCHEMA) [IF NOT EXISTS] database_name
  [COMMENT 'database_comment']
  [LOCATION 'cosn_location']
  [WITH DBPROPERTIES ('property_name' = 'property_value') [, ...]]
```

### Parameters\(参数\) {#parameters}

**\[IF NOT EXISTS\]**

Causes the error to be suppressed if a database named`database_name`already exists.

**\[COMMENT database\_comment\]**

Establishes the metadata value for the built-in metadata property named`comment`and the value you provide for`database_comment`. In AWS Glue, the`COMMENT`contents are written to the`Description`field of the database properties.

**\[LOCATION S3\_loc\]**

Specifies the location where database files and metastore will exist as`S3_loc`. The location must be an Amazon S3 location.

**\[WITH DBPROPERTIES \('property\_name' = 'property\_value'\) \[, ...\] \]**

Allows you to specify custom metadata properties for the database definition.

## Examples

```
ALTER TABLE customers PARTITION (zip='98040', state='WA') SET LOCATION 'cosn://mystorage/custdata/';
```



