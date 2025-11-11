#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-success-5144
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security 
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=5144""", """Message=A network share object was deleted.""", """SourceName =Microsoft Windows security auditing""", """Share Name:""", """TaskCategory=File Share""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
    """EventCode=({event_code}\d+)""",
    """ComputerName =({dest_host}({host}[^\s]+))""",
    """Keywords=({result}[^=]+?)\s+\w+=""",
    """Message=({event_name}[^:]+?)\s+\w+:""",
    """Security ID:\s+({user_sid}[^:]+?)\s+Account Name:""",
    """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Account Domain:\s+({domain}[^:]+?)\s+Logon ID:""",
    """Logon ID:\s+({login_id}[^\s]+)""",
    """Share Name:\s+(?:[\\\*]+)?({share_name}[^\s]+)""",
    """Share Path:\s+({share_path}[^\s]+)"""
    """Source Port(=|:)\s*({src_port}\d+)"""
  ]


}
```