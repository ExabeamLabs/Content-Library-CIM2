#### Parser Content
```Java
{
Name = "cisco-ise-cef-radius-traffic-success-cisepassedauth"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "epoch"
Conditions = [
  """CISE_Passed_Authentications"""
  """|Cisco|Cisco ISE|"""
  """CEF:"""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """ahost=({host}[^\s]+)"""
  """shost=({src_host}[^\s]+)"""
  """({event_name}CISE_Passed_Authentications)"""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """dhost=({dest_host}[^\s]+)"""
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
  """dst=({auth_server}[A-Fa-f:\d.]+)\s"""
  """dpt=({dest_port}\d+)"""
  """Cisco ISE\|(|[^\|]+)\|({event_code}\d+)\|"""
  """deviceSeverity=((?i)UNKNOWN|({severity}[^\s]+))"""
  """cs1=({auth_method}[^\s]+)"""
  """ad.User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """NetworkDeviceName\\*=({network}[^,\s]+)"""
  """dvchost=({dest_host}[^\s]+)"""
  """dvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
]
DupFields = [
  "dest_host->auth_server"
]
ParserVersion = "v1.0.0"


}
```