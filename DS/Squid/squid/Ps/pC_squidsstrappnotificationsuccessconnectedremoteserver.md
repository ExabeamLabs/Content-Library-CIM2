#### Parser Content
```Java
{
Name = "squid-s-str-app-notification-success-connectedremoteserver"
Vendor = "Squid"
Product = "Squid"
TimeFormat = "yyyy.MM.dd HH:mm:ss"
Conditions = [
"""LOG5["""
"""Service [squid]"""
"""connected remote server from"""
]
Fields = [
  """({time}\d\d\d\d\.\d\d\.\d\d \d\d:\d\d:\d\d) LOG5[^\]]+\]:\s.+?\[squid\]\s({event_name}connected remote server) from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```