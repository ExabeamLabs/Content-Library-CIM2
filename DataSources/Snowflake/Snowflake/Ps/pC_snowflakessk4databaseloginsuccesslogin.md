#### Parser Content
```Java
{
Name = snowflake-s-sk4-database-login-success-login
Vendor = Snowflake
Product = Snowflake
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ destinationServiceName =Snowflake"""
  """"EVENT_TYPE":"LOGIN""""
  """"FIRST_AUTHENTICATION_FACTOR":""""
]
Fields = [
  """"EVENT_TIMESTAMP":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"EVENT_ID":({query_id}\d+)"""
  """"USER_NAME":"({db_user}[^"]+)""""
  """"CLIENT_IP":"({src_ip}[\da-fA-F.:]+)""""
  """"REPORTED_CLIENT_TYPE":"({app}[^"]+)""""
  """"IS_SUCCESS":"({result}[^"]+)""""
  """\ssuser=(anonymous|({user}[^\s]+))"""
]
ParserVersion = "v1.0.0"


}
```