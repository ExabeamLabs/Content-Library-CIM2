#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4648"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
"""Exabeam Windows 4648"""
"""summary_windows_4648_data"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)"""
"""({event_code}4748)"""
"""summary_windows_4648_data="{1,20}\d+:\d+:\d+\s*\d+-\d+-\d+:::(-|({host}[^:::]+))?:::(-|({event_code}[^:::]+))?:::(-|({user_sid}[^:::]+))?:::(-|({user}[\w\.\-]{1,40}\$?))?:::(-|({domain}[^:::]+))?:::(-|({login_id}[^:::]+))?:::(-|({account}[^:::]+))?:::(-|({account_domain}[^:::]+))?:::(-|({dest_host}[\w\-.]+))?:::(-|({process_id}[^:::]+))?:::({process_path}({process_dir}(?:.+?)?[\\\/])?({process_name}[^\\\/:::]+))?:::"""
]
ParserVersion = "v1.0.0"


}
```