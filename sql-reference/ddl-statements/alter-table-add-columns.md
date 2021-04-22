# ALTER TABLE ADD COLUMNS {#alter-table-add-columns}

Creates one or more properties for a database.

向现有表中添加一列或多列。使用可选分区语法时，更新分区元数据。

## Synopsis\(文法\) {#synopsis}

```
ALTER TABLE table_name 
  ADD COLUMNS (col_name data_type) [RESTRICT | CASCADE];
```

### Parameters\(参数\) {#parameters}

**ADD COLUMNS \(col\_name data\_type \[,col\_name data\_type,…\]\)**

增加列给某个表，可以是一个列或者多个列。

**`col_name 列名`**

**`data_type 数据类型`**

## Examples

```
ALTER TABLE events ADD COLUMNS (eventowner string);

ALTER TABLE events ADD COLUMNS (eventowner string) CASCADE;
```



