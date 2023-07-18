#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-network-listen-5154
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """5154""", """The Windows Filtering Platform has permitted an application or service to listen on a port for incoming connections""" ]
  Fields = [
        """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
        """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
        """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
        """({event_code}5154)""",
        """({event_name}The Windows Filtering Platform has permitted an application or service to listen on a port for incoming connections)""",
        """Application Name:\s*(|-|({app}.+?))\s*Network Information""",
        """Source Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """Source Port:\s*({src_port}\d+)""",
        """Protocol:\s*({protocol}[^\s]+)""",
        """Process ID:\s*({process_id}\d+)""",
  ]


}
```