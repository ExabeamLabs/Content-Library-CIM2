#### Parser Content
```Java
{
Name = "sailpoint-securityiq-kv-file-delete-success-sharepoint"
Vendor = "Sailpoint"
Product = "SecurityIQ"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """| applicationtype : Sharepoint |"""
  """actiontype : Delete"""
]
Fields = [
  """creation_timestamp\s:\s({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{3})"""
  """ipaddress\s:\s({host}[^|]+)\s\|"""
  """ipaddress\s:\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? \|"""
  """userfullname\s:\s({user_sid}(?=[^\\]+\\)({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)|(?:.+?))\s\|"""
  """objectname\s:\s({file_name}[^|]+)\s\|"""
  """domain\s:\s({domain}[^|]+)\s\|"""
  """applicationtype\s:\s({app}[^|]+)\s\|"""
  """\spath\s:\s({file_dir}[^|]+)\s\|"""
  """fileextension\s:\s({file_ext}[^|]+)\s\|"""
  """actiontype\s:\s({access}({operation}[^\ ]+))(\s|\s\([^\)]+\)\s)\|"""
]
ParserVersion = "v1.0.0"


}
```