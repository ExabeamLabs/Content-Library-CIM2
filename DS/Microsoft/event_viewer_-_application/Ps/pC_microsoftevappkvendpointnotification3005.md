#### Parser Content
```Java
{
Name = microsoft-evapp-kv-endpoint-notification-3005
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Application
  TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [ """Event code: 3005""","""Process name:""","""Account name:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}\S+)\s({alert_severity}\S+)""",
    """Event time:\s*({time}\d+\/\d+\/\d\d\d\d\s\d+:\d\d:\d\d\s(AM|PM|am|pm))""",
    """Event code:\s*({event_code}\d+)""",
    """Event message:\s*({event_name}[^=]+?)\s*Event time:""",
    """Account name:\s*(({domain}[^\\]+)\\*)?({user}[\w\.\-]{1,40}\$?)""",
    """Process ID:\s({process_id}\d+)""",
    """Process name:\s+({process_name}[^=]+?)\s+Account name:""",
# application_path is removed
# request_url is removed
  ]


}
```