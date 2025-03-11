#### Parser Content
```Java
{
Name = "cisco-asa-kv-vpn-logout-success-28"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
  """ disconnected:  Session Type: """
  """AUTH/28"""
]
Fields = [
  """({time}\d+\/\d+\/\d+ \d+:\d+:\d+)"""
  """RPT=\d+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """User\s+\[({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```