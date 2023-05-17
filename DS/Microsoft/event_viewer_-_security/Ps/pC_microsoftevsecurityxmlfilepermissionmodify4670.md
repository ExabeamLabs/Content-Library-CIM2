#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-file-permission-modify-4670
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4670</EventID>""", """<Task>Authorization Policy Change""", """Permissions on an object were changed""" ]
  Fields = [
    """({event_name}Permissions on an object were changed)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z('|")\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """Subject:.+?Security ID:\s*({user_sid}[^\s]+)""",
    """Subject:\s*([^"]+?)Account Name:\s*(-|({user}[^\s]+))""",
    """Subject:\s*([^"]+?)Account Domain:\s*(-|({domain}[^\s]+))""",
    """Subject:\s*([^"]+?)Logon ID:\s*({login_id}[^\s]+)""",
    """Object:\s*.+?Object Server:\s*({object_server}[^\s]+)""",
    """Object:\s*([^$]+)Object Type:\s*({object_type}[^\s]+)""",
    """Object:\s*[^$]+Object Name:(-|({object_name}[^\s]+))""",
    """Process:\s*Process ID:\s*({process_id}[^\s]+)""",
    """Process:\s*([^$]+?)Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({process_name}[^\s\\\/]+))\s+Permissions Change:""",
    """<Data Name =('|")SubjectUserName('|")>({user}[^<]+)<"""
  ]
  DupFields = ["process_name -> file_name"]


}
```