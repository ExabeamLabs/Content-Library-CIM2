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
    """\Wrt=({time}\d+)""",
    """CEF:([^\|]*\|){5}({alert_type}[^\s:]+):?\s*\-?\s*({alert_name}[^\|]+)\|({alert_severity}\d+)""",
    """\WeventId=({alert_id}\d+)""",
    """\Wshost=({src_host}\S+)\s*(\w+=|$)""",
    """\Wdhost=({dest_host}\S+)\s*(\w+=|$)""",
    """\Wsrc=({src_ip}[\da-fA-F\.:]+)""",
    """\Wcs5=({src_ip}[\da-fA-F\.:]+)""",
    """\Wdst=({dest_ip}[\da-fA-F\.:]+)""",
    """\WdeviceSeverity=({alert_severity}.+?)\s*(\w+=|$)"""
  ]


}
```