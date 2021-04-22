# ALTER TABLE REPLACE COLUMNS {#alter-table-replace-columns}

Removes all existing columns from a table created with the  replaces them with the set of columns specified.You can use `ALTER TABLE REPLACE COLUMNS`to drop columns by specifying only the columns that you want to keep.

移除这个表中所有存在的列并用一个这个集合的列去替换原表中的列，你可以使用REPLACE语法来删除列并保留一些列。

## Synopsis\(文法\) {#synopsis}

```
ALTER TABLE table_name PARTITION (partition_spec) RENAME TO PARTITION (new_partition_spec)
```

### Parameters\(参数\) {#parameters}

`PARTITION (partition_col_name = partition_col_value [,...])`

Specifies a partition with the column name/value combinations that you specify. Enclose`partition_col_value`in quotation marks only if the data type of the column is a string.

`REPLACE COLUMNS (col_name data_type [,col_name data_type,…])`

Replaces existing columns with the column names and datatypes specified.

## Examples

```
ALTER TABLE tbl REPLACE COLUMNS (
            a  VARCHAR(100),
            b  VARCHAR(100),
            c  VARCHAR(100)
);
```

以下从orders表中查询删除的所有列，并使用emp替换列：

```
ALTER TABLE orders REPLACE COLUMNS 
(
    eid INT, 
    empid Int,
    ename STRING 
    name String
);
```



