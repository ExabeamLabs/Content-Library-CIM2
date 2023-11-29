#### Parser Content
```Java
{
Name = accellion-kw-json-app-activity-success-system
Conditions = [
  """url_host"""
  """app_host"""
  """description"""
  """System"""
  """event"""
]
DupFields = [
  "additional_info->operation"
]
ParserVersion = "v1.0.0"
},  
 
{
Vendor = Accellion
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """\w+\s+\d+ \d+:\d+:\d+\s+({host}[\w.\-]+)\s+"""
  """({host}[\w.\-]+)\s+rest_server.py:"""
  """\ssize=({bytes}\d+)"""
  """({email_address}[^@\s]+@({email_domain}[^\s]+))\s+id=[^,]+,\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,\s*Activity:?"""
  """Activity:\s*({operation}.+?)\."*\s*$"""
  """Activity Type:\s+({operation}[^\s,]+)"""
]
DupFields = [
  "host->dest_host"
]
Name = accellion-kw-kv-app-activity-success-viewedemailsubject
Product = Kiteworks
Conditions = [
  """Viewed an e-mail Subject"""
  """Activity:"""
]
ParserVersion = "v1.0.0"


}
```