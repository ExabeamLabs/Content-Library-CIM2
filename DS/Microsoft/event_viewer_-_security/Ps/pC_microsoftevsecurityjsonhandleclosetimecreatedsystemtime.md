#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-handle-close-timecreatedsystemtime
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """The handle to an object was closed""", """TimeCreated SystemTime""" ]
  Fields = [
    """(?i)\w+ \d+ \d\d:\d\d:\d\d (am|pm|\d{4}|({host}[\w\-.]+))\s""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+4658\s""",
    """({event_code}4658)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """({event_name}The handle to an object was closed)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Object:""",
    """Object Server:\s*({object_server}\S.*?)\s+Handle ID:""",
    """Process ID:\s*({process_id}[^\s]*)""",
    """Process Name:\s*({process_path}({process_dir}[^\s\\/]+?([/\\]+[^\\/:\*\?"<>\|]+?)*)[/\\]+({process_name}[^\\/:\*\?"<>\|]+?))(\s*$|(<|\s+\-\d+))"""
    """({operation_type}closed)""",
    """Handle ID:\s*({object_id}.+?)\s""",
  ]
  DupFields = [ "host->dest_host" ]


}
```