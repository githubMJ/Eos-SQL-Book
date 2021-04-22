# ALTER TABLE SET LOCATION {#alter-table-set-location}

Changes the location for the table named table\_name, and optionally a partition with partition\_spec.

改变表或者分区表的存储位置

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



