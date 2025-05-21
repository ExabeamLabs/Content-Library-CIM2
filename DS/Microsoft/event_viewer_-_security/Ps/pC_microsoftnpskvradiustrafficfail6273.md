#### Parser Content
```Java
{
Name = "microsoft-nps-kv-radius-traffic-fail-6273"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """LogName =Security""", """EventCode=6273""", """ComputerName =""", """SourceName =Microsoft Windows security auditing""" ]
  Fields = [
  """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d \w+) LogName ="""
  """ComputerName =({src_host}({host}[\w\-.]+))"""
  """({event_code}6273)"""
  """User:.+?Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """User:.+?Account Domain:\s*({domain}[\w\.\-]+)""",
  """Calling Station Identifier:\s*({src_mac}[^\s]+)"""
  """NAS IPv4 Address:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """NAS Port:\s*({dest_port}\d+)"""
  """Client Friendly Name:\s*({client}[\w\-\.]+)"""
  """Authentication Type:\s*({auth_type}[^\s]+)"""
  """Account Session Identifier:\s*({session_id}[^\s]+)"""
  """Reason Code:\s*({result_code}\d+)"""
  """Reason:\s*({failure_reason}[^\$]+?)\s*$"""
  """TaskCategory=({operation_type}[^=]+?)\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```