#### Parser Content
```Java
{
Name = cisco-asa-str-process-create-success-111009
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ "-111009", "%FTD-" ]
  Fields = [
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s*:\s*%FTD""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """User\s+'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """({event_name}executed)""",
    """ cmd:\s*({process_command_line}.+?)\s*$""",
  ]
  ParserVersion = "v1.0.0"


}
```