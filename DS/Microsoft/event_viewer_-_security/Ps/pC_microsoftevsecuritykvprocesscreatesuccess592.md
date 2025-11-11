#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-592
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=592""", """EventType=""", """A new process has been created""" ]
  Fields = [
    """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))""",
    """ComputerName =({dest_host}[\w\-.]+?)\s""",
    """({event_code}592)""",
    """User\s*Name:\s*(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Domain""",
    """Domain:\s*(?:-|({domain}.+?))\s+Logon""",
    """Logon\s*ID:\s*(?:-|({login_id}.+?))\s*$""",
    """New\s*Process\s*ID:\s*(?:-|({process_id}({process_guid}\d+)))\s""",
    """Creator\s*Process\s*ID:\s*(?:-|({parent_process_guid}\d+))\s""",
    """Image\s*File\s*Name:\s*({process_path}({process_dir}(?:[^\s]+)?[\\\/])?({process_name}[^\\\/\s]+))\s""",
    """Image\s*File\s*Name:\s*(?:-|({path}.+?))\s+Creator"""
    """({event_name}A new process has been created)"""
  ]
  ParserVersion = "v1.0.0"


}
```