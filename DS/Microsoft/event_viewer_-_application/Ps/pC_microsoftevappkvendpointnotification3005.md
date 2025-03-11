#### Parser Content
```Java
{
Name = microsoft-evapp-kv-endpoint-notification-3005
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Application
  ExtractionType = json
  TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """Event code: 3005""","""Process name:""","""Account name:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """"(?i)Computer(Name)?":\s*"({host}[^"]+)""""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}\S+)\s({alert_severity}\S+)""",
    """Event time:\s*({time}\d+\/\d+\/\d\d\d\d\s\d+:\d\d:\d\d\s(AM|PM|am|pm))""",
    """Event code:\s*({event_code}\d+)""",
    """Event message:\s*({event_name}[^=]+?)\s*Event time:""",
    """Account name:\s*(({domain}[^\\]+)\\*)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s|\\[rnt])+Exception information:""",
    """Process ID:\s({process_id}\d+)""",
    """Process name:\s+({process_name}[^=]+?)\s+Account name:""",
# application_path is removed
# request_url is removed
    """exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """exa_regex=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}\S+)\s({alert_severity}\S+)""",
    """exa_regex=Event time:\s*({time}\d+\/\d+\/\d\d\d\d\s\d+:\d\d:\d\d\s(AM|PM|am|pm))""",
    """exa_json_path=$.Id,exa_field_name=event_code"""
    """exa_json_path=$.Computer,exa_field_name=host"""
    """exa_regex=Event code:\s*({event_code}\d+)"""
    """exa_regex=Event message:\s*({event_name}[^=]+?)\s*Event time:"""
    """exa_regex=Account name:\s*(({domain}[^\\]+)\\*)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s|\\[rnt])+Exception information:""",
    """exa_regex=Process ID:\s({process_id}\d+)""",
    """exa_regex=Process name:\s+({process_name}[^=]+?)\s+Account name:""",
  ]


}
```