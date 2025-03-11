#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-network-listen-5154
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy"]
  Conditions = [ """5154""", """The Windows Filtering Platform has permitted an application or service to listen on a port for incoming connections""" ]
  Fields = [
        """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
        """"(TimeGenerated|created)":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
        """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
        """"Computer":"({host}[^"]+)"""",
        """({event_code}5154)""",
        """({event_name}The Windows Filtering Platform has permitted an application or service to listen on a port for incoming connections)""",
        """Application Name:(\s|\\[rnt])*(|-|({app}.+?))(\s|\\[rnt])*Network Information""",
        """Source Address:(\s|\\[rnt])*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """Source Port:(\s|\\[rnt])*({src_port}\d+)""",
        """Protocol:(\s|\\[rnt])*({protocol}[^\s]+?)(\s|\\[rnt])*Filter Information:""",
        """Process ID:(\s|\\[rnt])*({process_id}\d+)""",
  ]


}
```