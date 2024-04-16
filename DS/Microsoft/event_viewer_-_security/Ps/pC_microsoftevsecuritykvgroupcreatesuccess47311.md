#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-create-success-4731-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = ["""EventCode=4731""","""SourceName =Microsoft Windows security auditing.""","""TaskCategory="""]
  Fields = [
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
  """Computer(Name)?="?({host}[\w\-.]+)"?"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """LogName =({log_name}[^\s]+)"""
  """RecordNumber=({event_id}\d+)"""
  """EventCode=({event_code}\d+)"""
  """Message=({event_name}[^:\.]+?)(:|\.)"""
  """TaskCategory=({operation}[^=]+?)\s*(\w+=|$)"""
  """Keywords=(None|({result}[^=]+))\s\w+="""
  """SourceName =({service_name}.+?)(\.\s+\w+=|\s*$)"""
  """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}[\w\.\-]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}\S+))\s"""
  """Group Name:\s*(|-|({group_name}[^:]+?))\s+Group Domain:\s*(|-|({group_domain}[^\s]+))\s"""
  """Message=A security-enabled\s*({group_type}[^\s]+)\s+group was created."""
]


}
```