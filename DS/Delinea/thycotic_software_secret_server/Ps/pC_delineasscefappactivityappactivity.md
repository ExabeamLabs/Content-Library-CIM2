#### Parser Content
```Java
{
Name = delinea-ss-cef-app-activity-appactivity
  ParserVersion = v1.0.0
  Vendor = Delinea
  Product =  Thycotic Software Secret Server
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Thycotic Software|Secret Server|""" ]
  Fields = [
    """({host}[^\s]+) CEF""",
    """rt=({time}\w+ \d+ \d+ \d+:\d+:\d+)""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """msg=({event_name}.+?)\s*(:|\w+=)""",
    """msg=({additional_info}.+?)\s+(\w+=|$)""",
    """CEF:\d+\|([^\|]+\|){4}({category}[^\|]+)"""
    ]


}
```