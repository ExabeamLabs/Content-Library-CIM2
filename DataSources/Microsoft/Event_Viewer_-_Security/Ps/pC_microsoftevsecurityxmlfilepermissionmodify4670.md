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
    """<TimeCreated SystemTime='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """Subject:.+?Security ID:\s*({user_sid}[^\s]+)""",
    """Subject:.+?Account Name:\s*(-|({user}[^\s]+))""",
    """Subject:.+?Account Domain:\s*(-|({domain}[^\s]+))""",
    """Subject:.+?Logon ID:\s*({login_id}[^\s]+)""",
    """Object:.+?Object Server:\s*({object_server}[^\s]+)""",
    """Object:.+?Object Type:\s*({object_type}[^\s]+)""",
    """Object:.+?Object Name:\s*(-|({object_name}[^\s]+))""",
    """Process:.+?Process ID:\s*({process_id}[^\s]+)""",
    """Process:.+?Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({process_name}[^\s\\\/]+))\s+Permissions Change:""",
  ]
  DupFields = ["process_name -> file_name"]


}
```