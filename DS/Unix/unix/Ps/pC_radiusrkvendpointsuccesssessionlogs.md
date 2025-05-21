#### Parser Content
```Java
{
Name = "radius-r-kv-endpoint-success-sessionlogs"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
Conditions = [
  """RADIUS Session Logs"""
  """RADIUS.Acct-Framed-IP-Address="""
  """Common.Host-MAC-Address="""
]
Fields = [
  """Common\.Username=(?!host\/)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*,Common\.Service="""
  """Common\.Username=({user_type}host)\/({computer_name}.*?)\s*,Common\.Service="""
  """Common\.Service=({network}.*?)\s*,Common\.Roles="""
  """Common\.Host-MAC-Address=({src_mac}\w+)\s*,RADIUS\.Acct-Framed-IP-Address="""
  """RADIUS\.Acct-Framed-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Common.NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Common\.Request-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d[^\s]+)"""
]
DupFields = [
  "host->auth_server"
  "computer_name->user"
  "computer_name->dest_host"
]
ParserVersion = "v1.0.0"


}
```