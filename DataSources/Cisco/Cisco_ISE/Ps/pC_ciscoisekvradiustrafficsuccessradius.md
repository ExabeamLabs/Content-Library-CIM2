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
  """User-Name = "(({domain}[^\\"]+)\\+)?(?!((\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|((\w{2}:){5}\w{2})|(host\/)))({user}[^"]+)""""
  """NAS-Identifier = "({location}[^"]+)""""
  """Calling-Station-Id = "({src_mac}[^"]+)""""
  """NAS-IP-Address = ({dest_ip}[\da-fA-F\.:]+)"""
  """Framed-IP-Address = ({dest_ip}[\da-fA-F\.:]+)"""
]
ParserVersion = "v1.0.0"


}
```