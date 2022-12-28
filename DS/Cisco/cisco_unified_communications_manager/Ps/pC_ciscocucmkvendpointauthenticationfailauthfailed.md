#### Parser Content
```Java
{
Name = cisco-cucm-kv-endpoint-authentication-fail-authfailed
Vendor = Cisco
Product = Cisco Unified Communications Manager
TimeFormat = "MMM dd yyyy HH:mm:ss a"
Conditions = [
  """AuthenticationFailed: """
  """Login Authentication failed"""
  """App ID="""
]
Fields = [
  """\s({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))"""
  """UserID\s*=({user}[^\s\]]+)"""
  """Login IP Address\/Hostname\s*=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-.]+))"""
  """\]:\s*({additional_info}.+?)\.?\s+(\d+|\w+=)"""
  """App ID\s*=({app}[^\]]+)"""
]
ParserVersion = "v1.0.0"


}
```