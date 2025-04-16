#### Parser Content
```Java
{
Name = delinea-ss-cef-app-activity-appactivity
  ParserVersion = v1.0.0
  Vendor = Delinea
  Product =  Secret Server
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Thycotic Software|Secret Server|""" ]
  Fields = [
    """({host}[^\s]+) CEF""",
    """rt=({time}\w+ \d+ \d+ \d+:\d+:\d+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """msg=({event_name}.+?)\s*(:|\w+=|\w+:)""",
    """msg=({additional_info}.+?)\s+(\w+=|$)""",
    """CEF:\s*\d+\|([^\|]+\|){4}({category}[^\|]+)""",
    """Action:\s*\[({event_name}.+?)\]""",
    ]


}
```