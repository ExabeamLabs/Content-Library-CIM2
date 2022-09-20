#### Parser Content
```Java
{
Name = delinea-ss-cef-app-activity-appactivity
  ParserVersion = v1.0.0
  Vendor = Delinea
  Product = Secret Server
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Thycotic Software|Secret Server|""" ]
  Fields = [
    """({host}[^\s]+) CEF""",
    """rt=({time}\w+ \d+ \d+ \d+:\d+:\d+)""",
    """src=({src_ip}[A-Za-z0-9.\d]+)""",
    """msg=({event_name}.+?)\s*(:|\w+=)""",
    """msg=({additional_info}.+?)\s+(\w+=|$)""",
    """CEF:\d+\|([^\|]+\|){4}({category}[^\|]+)"""
    ]


}
```