#### Parser Content
```Java
{
Name = "oracle-db-kv-database-activity-success-connectdata"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "dd-MM-yyyy HH:mm:ss"
Conditions = [
  """CONNECT_DATA="""
  """SERVICE_NAME="""
  """INSTANCE_NAME="""
]
Fields = [
  """({time}\d+-\w+-\d+\s+\d\d:\d\d:\d\d)\s"""
  """PORT=({dest_port}\d+)"""
  """HOST=({dest_host}[\w\-.]+)\)\(USER="""
  """HOST=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\)\(PORT="""
  """PROGRAM=({process_name}[^\)]+)"""
  """PROTOCOL=({protocol}[^\)]+)"""
  """SERVICE_NAME=({app}[^\)]+)"""
  """USER=({user}[\w\.\-]{1,40}\$?)"""
  """\(PORT=\d+\)\)\s*\*\s*({result}[^\s\*]+)"""
]
ParserVersion = "v1.0.0"


}
```