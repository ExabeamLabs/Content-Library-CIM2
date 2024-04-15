#### Parser Content
```Java
{
Name = "unix-unix-kv-user-create-success-useradd-1"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"useradd""""
  """UID"""
  """"new user:"""
]
Fields = [
  """"+new user:\s+name\\=({account_name}[^\s,]+)"""
  """"+new user.+?UID\\=({account_id}[^\s,]+)"""
  """"+timestamp"+:"+({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)"""
  """requestClientApplication=({app}.+?)\s\w+="""
  """host"+:"+({host}[^"]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```