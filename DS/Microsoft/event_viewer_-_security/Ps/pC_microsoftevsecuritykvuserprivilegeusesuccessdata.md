#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-privilege-use-success-data"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
"""Exabeam Windows 4674"""
"""summary_windows_4674_data"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)"""
"""({event_code}4764)"""
"""summary_windows_4674_data=\"+\d+:\d+:\d+\s*\d+-\d+-\d+:::(-|({host}[\w\-.]+))?:::(-|({event_code}[^:::]+))?:::(-|({result}[^:::]+))?:::(-|({process_path}.+?))?:::(-|({process_dir}.+?))?:::(-|({process_name}.+?))?:::(-|({user}[\w\.\-]{1,40}\$?))?:::(-|({domain}[^:::]+))?:::(-|({login_id}[^:::]+))?:::(-|({object_server}[^:::]+))?:::(-|({object_type}[^:::]+))?:::(-|({object}.+?))?:::(-|({access}[^:::]+))?:::(-|({privileges}[^:::]+))?:::"""
]
DupFields = [
"host->dest_host"
"process_dir->directory"
]
ParserVersion = "v1.0.0"


}
```