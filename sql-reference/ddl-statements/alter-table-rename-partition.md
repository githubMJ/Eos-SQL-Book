# ALTER TABLE RENAME PARTITION {#alter-table-rename-partition}

Renames a partition column, partition\_spec, for the table named table\_name, to new\_partition\_spec.

重命名语法

## Synopsis\(文法\) {#synopsis}

```
ALTER TABLE table_name PARTITION (partition_spec) RENAME TO PARTITION (new_partition_spec)
```

### Parameters\(参数\) {#parameters}

**`PARTITION (partition_spec)`**

Rename a partition from an existing partition

重命名某个分区。

## Examples

```
ALTER TABLE tbl PARTITION (dt='2020-11-12') RENAME TO PARTITION (dt='2021-11-12');
```





