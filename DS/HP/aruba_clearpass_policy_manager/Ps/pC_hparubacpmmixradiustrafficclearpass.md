#### Parser Content
```Java
{
Name = "hp-arubacpm-mix-radius-traffic-clearpass"
Vendor = "HP"
Product = "Aruba ClearPass Policy Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
Conditions = [
  """0|Aruba Networks|ClearPass|"""
  """Common.NAS-IP-Address="""
  """Common.Host-MAC-Address="""
]
Fields = [
  """Common\.Request-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d[^\s]+)"""
  """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+(LEEF|CEF):"""
  """Common\.Username=(?:({user_type}host)\/)?(({email_address}[^@\s]+@[^\.\s]+\.[^\s]+)|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s\w+\.\w+=)"""
  """Common\.Service=({network}.*?)\s*([\w\-.]+=|$)"""
  """Common\.Host-MAC-Address=({src_mac}\w+)\s*([\w\-.]+=|$)"""
  """Common\.Auth-Type=(|({auth_type}.+?))\s*([\w\-.]+=|$)"""
  """Common\.NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """AD status:({failure_reason}[^\(]+)\s"""
]
DupFields = [
  "host->auth_server"
]
ParserVersion = "v1.0.0"


}
```