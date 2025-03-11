#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-scheduled-task-disable-4701
  Vendor = Microsoft
  Product = Event Viewer - Security
  Conditions = [ """EventCode=4701""", """ComputerName =""", """A scheduled task was disabled""" ]
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Fields = [
    """ComputerName =({host}[^\s]+)""",
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
    """({event_code}4701)""",
    """({event_name}A scheduled task was disabled)""",
    """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Account Domain:\s*({domain}[^\s:]+)""",
    """Logon ID:\s*({login_id}[^\s:]+)""",
    """Task Name:\s*({task_name}[^\s]+)\s*Task Content:""",   
    """Task Content:\s*({additional_info}.+?)$"""
  ]
  ParserVersion = v1.0.0


}
```