# DESCRIBE TABLE {#describe-table}

Shows the list of columns, including partition columns, for the named column. This allows you to examine the attributes of a complex column.

显示命名列的列列表，包括分区列。

## Synopsis\(文法\) {#synopsis}

```
DESCRIBE [EXTENDED | FORMATTED] [db_name.]table_name [PARTITION partition_spec];
```

### Parameters\(参数\) {#parameters}

**\[EXTENDED \| FORMATTED\]**

Determines the format of the output. If you specify`EXTENDED`, all metadata for the table is output in Thrift serialized form. This is useful primarily for debugging and not for general use. Use`FORMATTED`or omit the clause to show the metadata in tabular format.

**\[PARTITION partition\_spec\]**

If included, lists the metadata for the partition specified by`partition_spec`, where`partition_spec`is in the format`(partition_column = partition_col_value, partition_column = partition_col_value, ...)`.

## 

## Examples

```
ALTER TABLE customers PARTITION (zip='98040', state='WA') SET LOCATION 'cosn://mystorage/custdata/';
```



