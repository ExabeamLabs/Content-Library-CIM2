#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-success-5142
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security 
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """SourceName =Microsoft Windows security auditing""", """A network share object was added""", """EventCode=5142""", """Share Information:""" ]
  Fields = [
    """ComputerName =({host}[\w\-.]+)""",
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(am|AM|pm|PM))""",
    """({event_name}A network share object was added)""",
    """({event_code}5142)""",
    """Account Name:\s*({user}[^\s]+)""",
    """Account Domain:\s*({domain}[^\s]+)""",
    """Logon ID:\s*({login_id}[^\s]+)""",
    """Security ID:\s*(NT|({user_sid}[^\s]+))""",
    """Share Name:\s*[\\\*]*({share_name}[^:]+?)\s*Share Path:""",
    """Share Path:\s*(\s|({share_path}[^"]+?))\s*$""",
    """Keywords=({result}[^:=]+?)\s*\w+[:=]"""
  ]
  DupFields = [ "host->dest_host" ]


}
```