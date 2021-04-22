# ALTER TABLE ADD PARTITION {#alter-table-add-partition}

Creates one or more partition columns for the table.

为某个表创建一个或多个分区列。

## Synopsis\(文法\) {#synopsis}

```
ALTER TABLE table_name ADD [IF NOT EXISTS]
  PARTITION
  (partition_col1_name = partition_col1_value
  [,partition_col2_name = partition_col2_value]
  [,...])
  [LOCATION 'location1'];
```

### Parameters\(参数\) {#parameters}

**`[IF NOT EXISTS]`**

Causes the error to be suppressed if a partition with the same definition already exists.



**`PARTITION (partition_col_name = partition_col_value [,...])`**

Creates a partition with the column name/value combinations that you specify. Enclose`partition_col_value`in string characters only if the data type of the column is a string.

**`[LOCATION 'location']`**

Specifies the directory in which to store the partitions defined by the preceding statement.

## Examples

```
ALTER TABLE events ADD COLUMNS (eventowner string);

ALTER TABLE events ADD COLUMNS (eventowner string) CASCADE;
```



