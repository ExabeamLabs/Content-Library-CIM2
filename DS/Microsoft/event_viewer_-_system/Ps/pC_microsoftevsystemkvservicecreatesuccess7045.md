#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-service-create-success-7045
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """ EventCode=7045""", """A service was installed in the system.""" ]
  Fields = [
    """({event_name}A service was installed in the system)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))\s+LogName =""",
    """({event_code}7045)""",
    """ComputerName =({host}[\w\-.]+)""",
    """User=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Sid=({user_sid}[^\s]+)""",
    """Service Name:\s*(\\+r|\\+t|\\+n)*(({service_name}[^=:\\_]+?)(_[^"\<]+?)?)\s*(\\+r|\\+t|\\+n)*Service File"""
    """Service File Name:\s+(|-|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/\s]+)))\s+Service Type:""",
    """Service Type:\s+({service_type}.+?)\s+Service Start Type:""",
    """Service Account:\s+({account_name}.+?)\s*(\w+=|$)"""
    """Service File Name:\s*({process_command_line}[^=]+?)\s*Service Type:"""
  ]
  DupFields = [ "host->dest_host", "process_command_line->service_command_line" ]


}
```