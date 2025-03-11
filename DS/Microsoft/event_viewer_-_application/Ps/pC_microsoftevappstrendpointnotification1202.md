#### Parser Content
```Java
{
Name = microsoft-evapp-str-endpoint-notification-1202
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """1202""", """Security policies were propagated with warning""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """"TimeCreated":"[\\\/]*Date\(({time}\d{13})"""
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
    """"Computer":"({host}[\w\.\-]+)"""",
    """({event_code}1202)""",
    """({event_name}Security policies were propagated with warning)\.\s*({result_code}[\w]+)\s:"""
    """exa_json_path=$.Id,exa_field_name=event_code"""
    """exa_regex=({event_name}Security policies were propagated with warning)\.\s*({result_code}[\w]+)\s:"""
    """exa_json_path=$.MachineName,exa_field_name=host"""
    """exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """exa_regex="TimeCreated":"[\\\/]*Date\(({time}\d{13})"""
    """exa_regex=({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)"""
  ]


}
```