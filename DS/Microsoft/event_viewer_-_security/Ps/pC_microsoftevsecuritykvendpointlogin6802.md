#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-680-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyyMMddHHmmss.SSS"
Conditions = [
  """EventCode = 680;"""
  """Logon attempt by:"""
]
Fields = [
  """Computer(Name)? = "+({host}[^"]+)""""
  """({event_name}Logon attempt)"""
  """EventCode = ({event_code}\d+)"""
  """TimeGenerated = "({time}[\d]+.\d\d\d)"""
  """Logon account:\s+({user}[^@]+?)(?:@({domain}[^\s.]+)[^\s]*)?\s+Source Workstation:\s+({dest_host}[^\s]+)"""
  """Error Code:\s+({result_code}[\w\-]+)"""
]
ParserVersion = "v1.0.0"


}
```