#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-close-4658
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """The handle to an object was closed""" ]
  Fields = [
    """\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({dest_host}({host}[\w\-.]+)))\s""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+4658\s""",
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"(?i)HostName":\s*"({dest_host}({host}[^"]+))"""",
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
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s"""
  ]


}
```