#### Parser Content
```Java
{
Name = snowflake-s-sk4-database-query-success-queryhistory
Vendor = Snowflake
Product = Snowflake
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ destinationServiceName =Snowflake"""
  """QUERY_TYPE":""""
  """"QUERY_ID":""""
  """"QUERY_TEXT":""""
  """QUERY_HISTORY"""
]
Fields = [
  """"START_TIME":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"QUERY_ID":"({query_id}[^"]+)""""
  """"QUERY_TEXT":"({db_query}.+?)","""
  """"DATABASE_NAME":"({db_name}[^"]+)"""
  """"QUERY_TYPE":"(UNKNOWN|({db_operation}[^"]+))""""
  """"USER_NAME":"({db_user}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```