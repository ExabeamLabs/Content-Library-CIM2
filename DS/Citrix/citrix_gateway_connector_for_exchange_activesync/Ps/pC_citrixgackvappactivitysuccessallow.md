#### Parser Content
```Java
{
Name = "citrix-gac-kv-app-activity-success-allow"
Vendor = "Citrix"
Product = "Citrix Gateway Connector For Exchange ActiveSync"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Original Address="""
  """devicetype="""
  """agent="""
  """cmd="""
  """action=allow"""
]
Fields = [
  """Original Address=({host}[^\s]+)\s"""
  """action=({result}[^\s]+)\s"""
  """deviceid=({device_id}[^\s]+)\s"""
  """group=({group_name}[^\s]+)\s"""
  """user=({domain}[^\/]+)\\({user}[\w\.\-]{1,40}\$?)\s"""
  """devicetype=({device_type}[^\s]+)\s"""
  """cmd=({operation}[^\s]+)\s"""
  """agent=({user_agent}[^\s]+)\s"""
  """ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(?:\s|$)"""
  """user=({email_address}({user}[\w\.\-]{1,40}\$?)@[^@\s]+)\s"""
]
ParserVersion = "v1.0.0"


}
```