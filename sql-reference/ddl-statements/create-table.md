# CREATE TABLE {#create-table}

Creates a table with the name and the parameters that you specify.

创建一个表同时带一些属性。

## Synopsis\(文法\) {#synopsis}

```
CREATE EXTERNAL TABLE [IF NOT EXISTS]
 [db_name.]table_name [(col_name data_type [COMMENT col_comment] [, ...] )]
 [COMMENT table_comment]
 [PARTITIONED BY (col_name data_type [COMMENT col_comment], ...)]
 [ROW FORMAT row_format]
 [STORED AS file_format] 
 [WITH SERDEPROPERTIES (...)] ]
 [LOCATION 's3://bucket_name/[folder]/']
 [TBLPROPERTIES ( ['has_encrypted_data'='true | false',] ['classification'='aws_glue_classification',] property_name=property_value [, ...] ) ]
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
CREATE DATABASE db 
COMMENT 'db1_name' 
LOCATION 'cosn://path/to/db1' 
WITH DBPROPERTIES('k1' = 'v1','k2' = 'v2');
```

复杂创建方式：

```
CREATE TABLE t1 (
       ID  INTEGER
       NAME  STRING,
       HOBBY  ARRAY< STRING >,
       ADD  MAP< STRING, STRING >
)
ROW FORMAT DELIMITED
FIELDS TERMINATED BY ','
COLLECTION ITEMS TERMINATED BY '-'
MAP KEYS TERMINATED BY ':'
COMMENT 'db1_name' 
LOCATION 'cosn://path/to/db1' 
WITH DBPROPERTIES('k1' = 'v1','k2' = 'v2');
```



