#### Parser Content
```Java
{
Name = microsoft-evsecurity-mix-network-traffic-fail-5152
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """5152""", """The Windows Filtering Platform has blocked a packet""" ]
  Fields = [
    """({event_name}The Windows Filtering Platform has blocked a packet)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+)""",
    """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """({event_code}5152)""",
    """\sProcess ID:\s*(|-|({process_id}.+?))\s*Application Name:\s*(|-|({app}.+?))\s*Network Information""",
    """\s*Direction:\s*(|-|({direction}.+?))\s*Source Address:\s*(|-|0.0.0.0|(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Source Port:\s*(|-|({=src_port}\d+))\s*Destination Address:\s*(|-|0.0.0.0|(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s*Destination Port:\s*(|-|({=dest_port}\d+))\s*Protocol:\s*(|-|({protocol}.+?))\s*Filter Information:""",
  ]


}
```