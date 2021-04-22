# ALTER TABLE ADD COLUMNS {#alter-table-add-columns}

Creates one or more properties for a database.

向现有表中添加一列或多列。使用可选分区语法时，更新分区元数据。

## Synopsis\(文法\) {#synopsis}

```
ALTER TABLE table_name 
  [PARTITION 
   (partition_col1_name = partition_col1_value
   [,partition_col2_name = partition_col2_value][,...])]
  ADD COLUMNS (col_name data_type);
```

### Parameters\(参数\) {#parameters}

**PARTITION \(partition\_col\_name = partition\_col\_value \[,...\]\)**

Creates a partition with the column name/value combinations that you specify. Enclose`partition_col_value`in quotation marks only if the data type of the column is a string.

**ADD COLUMNS \(col\_name data\_type \[,col\_name data\_type,…\]\)**

Adds columns after existing columns but before partition columns.

## Examples

```
ALTER TABLE events ADD COLUMNS (eventowner string);

```



