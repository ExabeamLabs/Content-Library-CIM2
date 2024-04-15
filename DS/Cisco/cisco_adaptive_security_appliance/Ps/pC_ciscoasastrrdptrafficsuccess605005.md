#### Parser Content
```Java
{
Name = "cisco-asa-str-rdp-traffic-success-605005"
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """Login permitted from"""
  """-605005"""
  """%ASA-"""
]
Fields = [
  """({time}[a-zA-Z]{3}\s\d{2}\s\d{4}\s\d{2}:\d{2}:\d{2}):\s+"""
  """%(FTD|ASA)(-\w+)?-({priority}\d+)-({event_code}\d+)"""
  """\w+ \d+ \d+:\d+:\d+ ({host}[\w.\-]+)\s+:\s+%ASA"""  
  """Login permitted from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Login permitted from .+? to ({domain}[^:]+)"""
  """Login permitted from .+?:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Login permitted from .+? to .+?/({auth}.+?) for user"""
  """user "+(({domain}[^\\\/"]+)[\\\/]+)?({user}[^"]+)"""  
]
ParserVersion = "v1.0.0"


}
```