#### Parser Content
```Java
{
Name = cisco-fp-str-process-create-success-111008
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """-111008""", """%FTD-""" ]
  Fields = [
    """({time}\w+ \d+ (\d\d\d\d )?\d\d:\d\d:\d\d)\s(\w+\s)?({host}[\w\-.]+)\s*:\s*(\w+\s|%\w+\-)""",
    """\s(({host}[\w.\-]+))\s+:\s*(\w+\s|%\w+\-)""",
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """User\s+'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """({event_name}executed)\s+the\s+'({process_command_line}[^']+?)\s*'"""
  ]


}
```