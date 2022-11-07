#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-listen-5154
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>5154<""", """The Windows Filtering Platform has permitted an application or service to listen on a port for incoming connections""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """({event_name}The Windows Filtering Platform has permitted an application or service to listen on a port for incoming connections.)""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Data Name ='Protocol'>({protocol}[^<>]+?)<\/Data>""",
    """<Data Name ='SourceAddress'>({src_ip}[a-fA-F\d.:]+)""",
    """<Data Name ='SourcePort'>(0|({src_port}\d+))""",
    """<Data Name ='DestAddress'>({dest_ip}[a-fA-F\d.:]+)""",
    """<Data Name ='DestPort'>(0|({dest_port}\d+))""",
    """\sProcess ID:\s*(|-|({process_id}.+?))\s*Application Name:\s*(|-|({app}.+?))\s*Network Information"""
  ]


}
```