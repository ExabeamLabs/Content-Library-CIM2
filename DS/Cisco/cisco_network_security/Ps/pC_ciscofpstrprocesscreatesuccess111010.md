#### Parser Content
```Java
{
Name = cisco-fp-str-process-create-success-111010
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """-111010""", """%FTD-""" ]
  Fields = [
    """({time}\w+ \d+ (\d\d\d\d )?\d\d:\d\d:\d\d)\s(\w+\s)?({host}[\w\-.]+)\s*:\s*(\w+\s|%\w+\-)""",
    """\s(({host}[\w.\-]+))\s+:\s*(\w+\s|%\w+\-)""",
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """User\s+'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """({event_name}executed)\s+'({process_command_line}[^']+?)\s*'""",
    """from IP (0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]


}
```