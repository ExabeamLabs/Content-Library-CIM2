#### Parser Content
```Java
{
Name = snowflake-s-kv-database-login-success-login
Vendor = "Snowflake"
Product = "Snowflake"
TimeFormat = "epoch_sec"
Conditions = [
  """, USER_NAME=""""
  """ FIRST_AUTHENTICATION_FACTOR=""""
  """, EVENT_TYPE="LOGIN""""
]
Fields = [
  """EPOCH="({time}\d{10})"""
  """EVENT_ID="({query_id}\d+)",\s+EVENT_TIMESTAMP"""
  """USER_NAME="({db_user}[^"]+)""""
  """CLIENT_IP="({src_ip}[\da-fA-F.:]+)""""
  """REPORTED_CLIENT_TYPE="({app}[^"]+)""""
  """IS_SUCCESS="({result}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```