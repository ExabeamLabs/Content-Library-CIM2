#### Parser Content
```Java
{
Name = snowflake-s-sk4-database-login-success-login-1
Vendor = Snowflake
Product = Snowflake
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ destinationServiceName =Snowflake"""
  """"EVENT_TYPE":"LOGIN""""
  """.LOGIN_HISTORY"""
]
Fields = [
  """"EVENT_TIMESTAMP":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"EVENT_ID":({query_id}\d+)"""
  """"USER_NAME":"({db_user}[^"]+)""""
  """"CLIENT_IP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"REPORTED_CLIENT_TYPE":"({app}[^"]+)""""
  """"IS_SUCCESS":"({result}[^"]+)""""
  """\ssuser=(anonymous|({user}[^\s]+))"""
]
ParserVersion = "v1.0.0"


}
```