# Start spark shell
```shell
${SPARK_HOME}/bin/spark-shell --master "local[*]"  \
--confg spark.sql.warehouse.dir=${s3_warehouse_dir} \
"$@"
```

## within Spark shell
- assign value like `val tbl_name = "mydb.mytable"`
- run spark sql directly using `spark.sql($sql).show(false)`

## SQL 
### show schemas
```
show schemas;
use legacy_data_transfer;
```

### show tables
```
show tables;
```

### show table schema
```
describe formatted mytable;
show columns from mytable;
```

### show (all) partitions
```
show partitions mytable;
describe formatted mytable PARTITION(date="2020-10-31", hour=01);
```

### query data directly
```
select * from mytable where date=20210421 limit 1;
select * from mytable limit 1;
```

### show & update table properties
```
SHOW TBLPROPERTIES $tbl_name
-- SET TABLE COMMENT Using SET PROPERTIES
ALTER TABLE dbx.tab1 SET TBLPROPERTIES ('comment' = 'A table comment.');
-- DROP TABLE PROPERTIES
ALTER TABLE dbx.tab1 UNSET TBLPROPERTIES ('winner');
```



### drop partitions
```
ALTER TABLE mytable DROP IF EXISTS partition (environment="prod");
```

### drop table
```
DROP TABLE mytable;
```