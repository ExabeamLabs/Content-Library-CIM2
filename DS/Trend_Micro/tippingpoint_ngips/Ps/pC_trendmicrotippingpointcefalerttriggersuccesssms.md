#### Parser Content
```Java
{
Name = trendmicro-tippingpoint-cef-alert-trigger-success-sms
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = TippingPoint NGIPS
  TimeFormat = "epoch"
  Conditions = [ """|TippingPoint|SMS|""", """eventId=""" ]
  Fields = [
    """\Wdvc=({host}\S+)\s*(\w+=|$)""",
    """\Wdvchost=({host}\S+)\s*(\w+=|$)""",
    """\Wrt=({time}\d{13})""",
    """CEF:([^\|]*\|){5}({alert_type}[^\s:]+):?\s*\-?\s*({alert_name}[^\|]+)\|({alert_severity}\d+)""",
    """\WeventId=({alert_id}\d+)""",
    """\Wshost=({src_host}\S+)\s*(\w+=|$)""",
    """\Wdhost=({dest_host}\S+)\s*(\w+=|$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wcs5=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\WdeviceSeverity=({alert_severity}.+?)\s*(\w+=|$)"""
  ]


}
```