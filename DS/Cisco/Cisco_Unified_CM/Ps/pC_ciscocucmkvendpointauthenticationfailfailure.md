#### Parser Content
```Java
{
Name = cisco-cucm-kv-endpoint-authentication-fail-failure
Vendor = Cisco
Product = Cisco Unified CM
TimeFormat = "MMM dd yyyy HH:mm:ss a"
Conditions = [
  """EventType =UserLogging"""
  """EventStatus =Failure"""
  """Failed to Log into Cisco CCM Webpages"""
]
Fields = [
  """\s({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))"""
  """UserID\s*=({user}[^\s\]]+)"""
  """ClientAddress\s*=({src_ip}[A-Fa-f:\d.]+)"""
  """EventType\s*=({operation}[^\]]+)"""
  """ResourceAccessed\s*=({object}[^\]]+)"""
  """EventStatus\s*=({result}[^\]]+)"""
  """ComponentID\s*=({target}[^\]]+)"""
  """AuditDetails\s*=({event_name}[^\]]+)"""
  """Node ID=({dest_host}[^\]]+)"""
  """App ID\s*=({app}[^\]]+)"""
]
ParserVersion = "v1.0.0"


}
```