# ALTER TABLE DROP PARTITION {#alter-table-drop-partition}

Drops one or more specified partitions for the named table.

从表中删除一个或者多个分区。

## Synopsis\(文法\) {#synopsis}

```
ALTER TABLE table_name DROP [IF EXISTS] PARTITION (partition_spec) [, PARTITION (partition_spec)];
```

### Parameters\(参数\) {#parameters}

**`[IF EXISTS]`**

Suppresses the error message if the partition specified does not exist.

如果指定的分区不存在，则取消显示错误消息。

**`PARTITION (partition_spec)`**

Each`partition_spec`specifies a column name/value combination in the form`partition_col_name = partition_col_value [,...]`.

遍历每个分区列名属性和值从分区属性中并合并。

## Examples

```
ALTER TABLE tbl DROP IF EXISTS PARTITION (P = 1);
```

```
alter table tbl drop 
    partition (p1='a',p2=1), partition(p1='b',p2=2), 
    partition(p1='c',p2=3);
```



