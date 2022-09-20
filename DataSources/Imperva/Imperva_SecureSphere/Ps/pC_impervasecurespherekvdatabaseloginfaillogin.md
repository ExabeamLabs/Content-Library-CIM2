#### Parser Content
```Java
{
Name = imperva-securesphere-kv-database-login-fail-login
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "dd MMM yyyy HH:mm:ss"
Conditions = [
  """ os_user="""
  """ dbName ="""
  """ operation=Login"""
]
Fields = [
  """event_time=({time}\d\d \w+ \d\d\d\d \d\d:\d\d:\d\d)"""
  """\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-.]+)"""
  """user=({db_user}[^\s]+)"""
  """os_user=({user}[^\s]+)"""
  """source_ip=({src_ip}[A-Fa-f:\d.]+)"""
  """destination_ip=({dest_ip}[A-Fa-f:\d.]+)"""
  """dbName =({db_name}.+?)\s*(\w+=|$)"""
  """sqlError="({failure_reason}[^"]+?)""""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```