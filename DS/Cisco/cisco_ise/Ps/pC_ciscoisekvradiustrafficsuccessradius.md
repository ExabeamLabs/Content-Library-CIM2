#### Parser Content
```Java
{
Name = cisco-ise-kv-radius-traffic-success-radius
Vendor = Cisco
Product = Cisco ISE
TimeFormat = "epoch_sec"
Conditions = [
  "Acct-Authentic = RADIUS"
  "Acct-Status-Type = Start"
  "Acct-Unique-Session-Id ="
]
Fields = [
  """Timestamp = ({time}\d{10})"""
  """User-Name = "(({domain}[^\\"]+)\\+)?(?!((\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|((\w{2}:){5}\w{2})|(host\/)))({user}[\w\.\-]{1,40}\$?)""""
  """NAS-Identifier = "({location}[^"]+)""""
  """Calling-Station-Id = "({src_mac}[^"]+)""""
  """NAS-IP-Address = ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Framed-IP-Address = ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```