#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-network-listen-5154
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """5154""", """The Windows Filtering Platform has permitted an application or service to listen on a port for incoming connections""" ]
  Fields = [
        """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
        """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
        """({event_code}5154)""",
        """({event_name}The Windows Filtering Platform has permitted an application or service to listen on a port for incoming connections)""",
        """Application Name:\s*(|-|({app}.+?))\s*Network Information""",
        """Source Address:\s*({src_ip}[a-fA-F\d.:]+)""",
        """Source Port:\s*({src_port}\d+)""",
        """Protocol:\s*({protocol}[^\s]+)""",
        """Process ID:\s*({process_id}\d+)""",
  ]


}
```