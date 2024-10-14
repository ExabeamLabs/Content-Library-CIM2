#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4776-4"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
"""Exabeam Windows 4776"""
"""summary_windows_4776_data"""
]
Fields = [
"""search_time=({time}\d+)"""
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)"""
"""({event_code}4776)"""
"""summary_windows_4776_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({event_code}[^:::]+)?:::({dest_host}[\w\-.]+)?:::({result_code}[^:::]+)?:::({user}[\w\.\-\!\#\^\~]{1,40}\$?)?:::([^:::]+):::"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```