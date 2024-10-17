#### Parser Content
```Java
{
Name = cisco-cucm-kv-endpoint-login-success-userlogging
Vendor = Cisco
Product = Cisco Unified Communications Manager
TimeFormat = "MMM dd yyyy hh:mm:ss a"
Conditions = [
  """EventType =UserLogging"""
  """EventStatus =Success"""
  """Successfully Logged into Cisco CCM Webpages"""
]
Fields = [
  """\s({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))"""
  """UserID\s*=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """ClientAddress\s*=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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