#### Parser Content
```Java
{
Name = "oracle-db-cef-database-modify-success-update"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "epoch"
Conditions = [
  """|Oracle|FGA|"""
  """|UPDATE|"""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wshost=({src_host}[\w\-.]+)"""
  """\Wdhost=({dest_host}[\w\-.]+)"""
  """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\Wduser=({db_user}[^\s]+)"""
  """\Wcs3=({db_name}[^\s]+)"""
  """CEF:([^\|]*\|){5}({db_operation}[^\|]+)"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```