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
    """Subject:.+?Security ID:\s*(\\t|\\r|\\n)*({user_sid}[^\s\\"]+)\s*(\\t|\\r|\\n)*""",
    """Subject:\s*([^"]+?)Account Name:\s*(-|({user}[\w\.\-]{1,40}\$?))""",
    """Subject:\s*([^"]+?)Account Domain:(\\t|\\r|\\n|\s)*(|-|({domain}.+?))(\\t|\\r|\\n|\s)*Logon ID:""",
    """Subject:\s*([^"]+?)Logon ID:(\\t|\\r|\\n|\s)*({login_id}[^\s\\]+)(\\t|\\r|\\n|\s)*""",
    """Object Server:\s*((?-i)\\+[rnt])*({object_server}[^:]+?)[\\rnt\s]*Object Type:""",
    """Object Type:(\\t|\\r|\\n)*\s*(|({object_type}[^:]+?))(\\t|\\r|\\n)*\s*Object Name:""",
    """Object:\s*[^$]+Object Name:(\\t|\\r|\\n|-)*\s*(-|({object_name}[^:"]+?))\s""",
    """Process:\s*Process ID:\s*({process_id}[^\s]+)""",
    """Process:\s*([^$]+?)Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({process_name}[^\s\\\/]+))\s+Permissions Change:""",
    """<Data Name =('|")SubjectUserName('|")>({user}[\w\.\-]{1,40}\$?)<""",
    """Permissions Change:(\\+[rnt]|\s)*({attribute}[^<]+?)\s*<""",
    """Permissions Change:[\s\S]*?New Security Descriptor:\s*(\\t|\\r|\\n)*({permissions}[^<]+?)\s*<""",
    """<Data Name(\\)?=(\\)?("|')+ObjectName(\\)?("|')+>(-|({file_path}({file_dir}.+?)[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?))|[^\\:<]+)<\/Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = ["process_name -> file_name"]


}
```