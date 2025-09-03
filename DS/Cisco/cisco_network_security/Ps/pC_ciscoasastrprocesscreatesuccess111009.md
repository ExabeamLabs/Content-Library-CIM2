#### Parser Content
```Java
{
Name = cisco-asa-str-process-create-success-111009
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ "-111009", "%FTD-" ]
  Fields = [
    """({time}\w+ \d+ (\d\d\d\d )?\d\d:\d\d:\d\d)\s(\w+\s)?({host}[\w\-.]+)\s*:\s*(\w+\s|%\w+\-)""",
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """User\s+'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """({event_name}executed)""",
    """ cmd:\s*({process_command_line}.+?)\s*$""",
  ]
  ParserVersion = "v1.0.0"


}
```