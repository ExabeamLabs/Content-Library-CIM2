#### Parser Content
```Java
{
Name = "synologynas-s-str-share-access-success-connection"
Vendor = "Synology NAS"
Product = "Synology NAS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  " Connection "
  "accessed the shared folder"
]
Fields = [
  """>\w+ \d\d \d\d:\d\d:\d\d\s+({host}\S+)"""
  """Connection\s+(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?),"""
  """({protocol}\S+)\s+client\s+\[(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\]"""
  """from .*?IP:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """accessed the shared ({file_type}folder) \[(?:[\\\*]+)?({share_name}.+?)\]"""
]
ParserVersion = "v1.0.0"


}
```