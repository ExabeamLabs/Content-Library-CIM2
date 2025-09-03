#### Parser Content
```Java
{
Name = trendmicro-scanmail-cef-configuration-modify-300101
  Vendor = Trend Micro
  Product = Trend Micro ScanMail
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Trend Micro|SMEX|""", """|300101|Event Tracking|""" ]
  Fields = [
    """rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """shost=({host}[^\s=]+)\s+\w+=""",
    """CEF:([^\|]*\|){6}({severity}[^|]+)""",
    """CEF:([^\|]*\|){5}({category}[^|]+)""",
    """CEF:([^\|]*\|){4}({event_code}[^|]+)""",
    """({app}SMEX)""",
    """suser=(({domain}[^\\;]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
    """eventType=({operation}[^=]+)\s+\w+=""",
    """msg=({additional_info}[^=.]+)(\s+\w+=|\s*$)"""
    ]


}
```