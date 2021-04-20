# SHOW PARTITIONS {#show-partitions}

Lists all the partitions in a table.

列出表中的所有分区。

## Synopsis\(文法\) {#synopsis}

```
SHOW PARTITIONS [db_name.]table_name [PARTITION(partition_spec)];
```

### Parameters\(参数\) {#parameters}

`TABLE  [db_name.]table_name`

 表名。

`[PARTITION(partition_spec)]`

 分区列，可以有多个分区列条件。

## Examples {#examples}

```
SHOW PARTITIONS db01.table PARTITION(ds='2010-03-03', hr='12');
```



