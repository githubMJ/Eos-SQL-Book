# DESCRIBE TABLE {#describe-table}

Determines the format of the output. If you specify EXTENDED, all metadata for the table is output in Thrift serialized form. This is useful primarily for debugging and not for general use. UseFORMATTEDor omit the clause to show the metadata in tabular format.

明确表的输出格式。如果指定`EXTENDED`，则表的所有元数据都以旧格式序列化的形式输出。这主要用于调试，而不是一般用途。使用formatted或省略子句以表格格式显示元数据。

## Synopsis\(文法\) {#synopsis}

```
DESCRIBE [EXTENDED | FORMATTED] [db_name.]table_name [PARTITION partition_spec];
```

### Parameters\(参数\) {#parameters}

**`[EXTENDED | FORMATTED]`**

Determines the format of the output with table.

指定表的格式化形式。

**`[PARTITION partition_spec]`**

If included, lists the metadata for the partition specified by`partition_spec`, where`partition_spec`is in the format`(partition_column = partition_col_value, partition_column = partition_col_value, ...)`.

所有分区元数据列表。

## Examples

```
DESCRIBE tbl;

DESCRIBE FORMATTED tbl PARTITION (date_id = '2019-01-07');
```



