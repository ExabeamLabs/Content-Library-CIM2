#### Parser Content
```Java
{
Name = oracle-o-kv-database-login-success-dbx
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """SESSIONID="""
  """Authenticated by"""
  """DBID="""
]
Fields = [
  """NTIMESTAMP\#="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
  """USERID="({db_user}[^"]+)"""
  """USERHOST="({src_host}[^"]+)"""
  """RETURNCODE="({result}[^"]+)"""
  """Client address.+?\(PROTOCOL=({protocol}[^\)]+)"""
  """Client address.+?\(HOST=({src_ip}[A-Fa-f:\d.]+)"""
  """SPARE1="({user}[^"]+)"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```