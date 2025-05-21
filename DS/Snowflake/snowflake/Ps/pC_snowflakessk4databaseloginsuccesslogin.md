#### Parser Content
```Java
{
Name = snowflake-s-sk4-database-login-success-login
Vendor = Snowflake
Product = Snowflake
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """IS_SUCCESS:""",  """EVENT_TYPE:LOGIN""", """USER_NAME:""", """REPORTED_CLIENT_TYPE:""" ]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """cat=({category}[^,\s\|]+)"""
  """USER_NAME:({db_user}[^",:]+)"""
  """REPORTED_CLIENT_TYPE:({app}[^,"]+)"""
  """IS_SUCCESS:({result}[^,"]+)"""
  """\ssuser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """EVENT_TYPE:({event_name}[^,"]+)"""
]
ParserVersion = "v1.0.0"


}
```