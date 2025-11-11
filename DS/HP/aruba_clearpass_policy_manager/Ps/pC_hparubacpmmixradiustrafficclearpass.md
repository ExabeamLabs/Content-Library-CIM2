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
  """({auth_server}({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\s+(LEEF|CEF):"""
  """Common\.Username=(({user_type}host)\/({src_host}[\w\-.]+)|([\d]{14})|({auth_server}({host}[A-Z\d]{15}))|({=auth_server}({=host}[A-Z\d]{10}))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({src_mac}([a-fA-F\d]{2}[\-:]?){5}[a-fA-F\d]{2})|({user}[a-z\.\-\!\#\^\~]{1,40}\$?)@({domain}[^=]+)|(({=domain}[^\\\s]+)\\+)?({=user}[a-z\.\-\!\#\^\~]{1,40}\$?))(\s+\w+\.\w+=)"""
  """Common\.Service=({network}.*?)\s*([\w\-.]+=|$)"""
  """Common\.Host-MAC-Address=({src_mac}\w+)\s*([\w\-.]+=|$)"""
  """Common\.Auth-Type=(|({auth_type}.+?))\s*([\w\-.]+=|$)"""
  """Common\.NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """AD status:({failure_reason}[^\(]+)\s"""
]
ParserVersion = "v1.0.0"


}
```