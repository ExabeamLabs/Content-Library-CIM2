#### Parser Content
```Java
{
Name = snowflake-s-sk4-database-login-success-login-1
Vendor = Snowflake
Product = Snowflake
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss.SSS" ]
Conditions = [ """"IS_SUCCESS":"""",  """"EVENT_TYPE":"LOGIN"""", """"USER_NAME":"""", """"REPORTED_CLIENT_TYPE":"""" ]
Fields = [
  """"EVENT_TIMESTAMP":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"EVENT_TIMESTAMP":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)"""
  """"EVENT_ID":({query_id}\d+)"""
  """"USER_NAME":"({db_user}[^"]+)""""
  """"CLIENT_IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"REPORTED_CLIENT_TYPE":"({app}[^"]+)""""
  """"IS_SUCCESS":"({result}[^"]+)""""
  """"USER_NAME":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""  
  """\ssuser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """"ERROR_MESSAGE":"({failure_reason}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```