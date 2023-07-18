#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-request-4661
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """4661""", """A handle to an object was requested""" ]
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s+EvntSLog""",
    """({event_code}4661)""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"(?i)HostName":\s*"({host}[^"]+)"""",
    """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_name}A handle to an object was requested)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*({user}\S+)\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Object:""",
    """Object Server:\s*({object_server}\S.*?)\s+Object Type:""",
    """Object Type:\s*({object_type}\S+)\s*Object Name:""",
    """Object Name:\s*({object}\S.*?)\s*Handle ID:""",
    """Handle ID:\s*({handle_id}\S+)""",
    """Process ID:\s*({process_id}[^\s]*)""",
    """Process Name:\s*({process_path}({process_dir}.+?)[\\\/]({process_name}[^\\\/]+?))\s*Access Request Information:""",
    """Transaction ID:\s*\{({transaction_id}[^\s\}]+)\}?\s*Accesses:""",
    """Accesses:\s*({access}\S.*?)\s*Access Reasons:""",
    """Access Reasons:\s*(-|({access}\S.*?))\s*Access Mask:""",
    """Privileges Used for Access Check:.*?Properties:[\s\-]*(-|({privileges}.*?))\s*Restricted SID Count:""",
    """({operation_type}requested)""",
  ]


}
```