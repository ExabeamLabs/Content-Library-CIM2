#### Parser Content
```Java
{
Name = snowflake-s-sk4-database-query-success-queryhistory
Vendor = Snowflake
Product = Snowflake
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [  """QUERY_TYPE":"""", """"QUERY_ID":"""", """"QUERY_TEXT":"""", """QUERY_HISTORY""", """DATABASE_NAME""" ]
Fields = [
  """"START_TIME":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"QUERY_ID":"({query_id}[^"]+)""""
  """"QUERY_TEXT":"({db_query}.+?)","""
  """"SCHEMA_NAME":"({db_schema}[^"]+)""""
  """"WAREHOUSE_NAME":"({db_name}[^"]+)""""
  """"DATABASE_NAME":"({db_name}[^"]+)"""
  """"QUERY_TEXT":"({db_operation}(?i)(insert|delete|truncate|drop|alter|create|update|enable|disable|merge|select|dbcc))"""
  """"QUERY_TYPE":"(UNKNOWN|({db_operation}[^"]+))""""
  """"USER_NAME":"({db_user}[^"]+)""""
  """"ROLE_NAME":"({role}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```