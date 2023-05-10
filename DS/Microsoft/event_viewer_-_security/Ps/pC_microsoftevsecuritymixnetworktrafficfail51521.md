#### Parser Content
```Java
{
Name = microsoft-evsecurity-mix-network-traffic-fail-5152-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """"EventID":"5152"""", """<Data Name ='""" ]
  Fields = [
    """"Activity":"({event_name}[^"]+)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({host}[^"]+)""",
    """"EventID":"({event_code}\d+)""",
    """<Data Name ='Direction'>({direction}[^<>]+?)</Data>""",
    """<Data Name ='SourceAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Data Name ='SourcePort'>(0|({src_port}\d+))""",
    """<Data Name ='DestAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name ='DestPort'>(0|({dest_port}\d+))""",
    """<Data Name ='Protocol'>({protocol}[^<>]+?)</Data>"""
  ]


}
```