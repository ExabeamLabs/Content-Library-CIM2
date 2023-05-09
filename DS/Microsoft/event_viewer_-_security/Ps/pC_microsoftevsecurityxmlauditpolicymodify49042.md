#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-audit-policy-modify-4904-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """An attempt was made to register a security event source""", """4904""" ]
  Fields = [
    """({event_name}An attempt was made to register a security event source)""",
    """<Computer>(::ffff:)?({host}[^<]+)</Computer>""",
    """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)""",
    """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))"""
    """({event_code}4904)""",
    """\sAccount Name:\s*(|-|({user}.+?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*Process:""",
    """\sProcess ID:\s*(|-|({process_id}.+?))\s*Process Name:\s*(|-|({process_path}({process_dir}.*?)({process_name}[^\\\/]+?)))\s*Event Source:""",
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  ]
  DupFields = [ "host-> dest_host" ]


}
```