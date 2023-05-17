#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-4985
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """The state of a transaction has changed""", """4985""", """Account Name:""" ]
  Fields = [
    """({event_name}The state of a transaction has changed)""",
    """<Computer>(::ffff:)?({dest_host}({host}[^<]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """\Wrt=({time}\d+)""",
    """SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)""",
    """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))""",
    """({event_code}4985)""",
    """Subject:.+?\sSecurity ID:\s*(|-|SYSTEM|({user_sid}.+?))\s*Account Name:\s*(|-|SYSTEM|({user}.+?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*Transaction Information:\s*(|-|(.+?))\s*RM Transaction ID:\s*\{?(|-|(.+?))\}?\s*New State:\s*(|-|(.+?))\s*Resource Manager:\s*\{?(|-|(.+?))\}?\s*Process Information:\s*(|-|(.+?))\s*Process ID:\s*(|-|({process_id}.+?))\s*Process Name:\s*(|-|({process_path}({process_dir}.*?)({process_name}[^\\\/]+?)))\s*($|<|User:)""",
# DL Fields are removed
    """ComputerName:\s*(::ffff:)?({host}[\w.\-]+)""",
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  ]


}
```