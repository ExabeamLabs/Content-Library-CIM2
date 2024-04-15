#### Parser Content
```Java
{
Name = "openvpn-sslvpn-kv-app-authentication-fail-authfailed"
Vendor = "Open VPN"
Product = "Open VPN"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """AUTH_FAILED"""
  """openvpn"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d+)"""
  """(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\s\d+\s\d+:\d+:\d+\s\d+.*?({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}):({src_port}\d+).*?\[({user}[^\]]+)"""
  """SESSION:({additional_info}[^']+)"""
  """status=({action}\d+)"""
]
ParserVersion = "v1.0.0"


}
```