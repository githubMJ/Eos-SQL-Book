# DESCRIBE TABLE {#describe-table}

Shows the list of columns, including partition columns, for the named column. This allows you to examine the attributes of a complex column.

显示命名列的列列表，包括分区列。

## Synopsis\(文法\) {#synopsis}

```
ALTER TABLE table_name [ PARTITION (partition_spec) ] SET LOCATION 'new location';
```

### Parameters\(参数\) {#parameters}

**PARTITION \(partition\_spec\)**

Specifies the partition with parameters`partition_spec`whose location you want to change. The`partition_spec`specifies a column name/value combination in the form`partition_col_name = partition_col_value`.

改变某个分区列的位置。

`partition_col_name 分区列名`

`partition_col_value 分区列的值`

**SET LOCATION 'new location'**

Specifies the new location, which must be an Tencent COS location.

创建在一个新位置在tencent cos上

## Examples

```
ALTER TABLE customers PARTITION (zip='98040', state='WA') SET LOCATION 'cosn://mystorage/custdata/';
```



