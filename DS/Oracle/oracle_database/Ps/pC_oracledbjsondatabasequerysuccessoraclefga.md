#### Parser Content
```Java
{
Name = "oracle-db-json-database-query-success-oraclefga"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""OracleFGA""""
""""sqlText":"""
]
Fields = [
""""objName":"({db_object}[^"]+)"""
""""sqlText":"({db_query}.*?)",""""
""""objSchema":"({db_schema}[^"]+)"""
""""@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
""""srcHostname":"(({domain}[^"\\\/]+)[\\\/]+)?({src_host}[^"]+)"""
""""action":"({db_operation}[^"]+)"""
""""instanceName":"({db_name}[^"]+)"""
""""suUserID":"({user}[^"]+)"""
""""userID":"({db_user}[^"]+)"""
]
DupFields = [
"user->user"
]
ParserVersion = "v1.0.0"


}
```