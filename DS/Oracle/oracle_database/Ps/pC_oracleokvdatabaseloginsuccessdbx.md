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
  """Client address.+?\(HOST=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """SPARE1="({user}[\w\.\-]{1,40}\$?)"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```