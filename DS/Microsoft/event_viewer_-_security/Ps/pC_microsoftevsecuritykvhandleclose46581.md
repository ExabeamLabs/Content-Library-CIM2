#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-close-4658-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [ """The handle to an object was closed""", """Computer""", """TimeCreated SystemTime""" ]
  Fields = [
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """({event_code}4658)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """({event_name}The handle to an object was closed)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Object:""",
    """Object Server:\s*({object_server}\S.*?)\s+Handle ID:""",
    """Process ID:\s*[\\t]*({process_id}[^\s\\]*)""",
    """Process Name:\s*({process_path}({process_dir}[^\s\\/]+?([/\\]+[^\\/:\*\?"<>\|]+?)*)[/\\]+({process_name}[^\\/:\*\?"<>\|]+?))(\s*$|(<|\s+\-\d+))"""
    """({operation_type}closed)""",
    """Handle ID:\s*[\\t]*({object_id}.+?)[rnt\\]*Process Information""",
  ]
  DupFields = [ "host->dest_host" ]


}
```