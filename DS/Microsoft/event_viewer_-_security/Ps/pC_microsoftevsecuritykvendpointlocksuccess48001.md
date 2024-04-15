#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-lock-success-4800-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""The workstation was locked"""
"""4800"""
]
Fields = [
"""({event_name}The workstation was locked)"""
"""({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})"""
"""(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
"""(?i)(((audit|success)( |_)(success|audit))|information)(<\d+>|\s+)({host}[\w\-.]+)"""
"""Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({host}[\w.\-]+))"""
"""({event_code}4800)"""
"""Account Name:\s*({user}.+?)[\\n\s]*Account Domain"""
"""Account Domain:\s*({domain}[^\s]+)[\\n\s]*Logon ID"""
"""Logon ID:\s*({login_id}[^\s]+?)[\\n\s]+Session"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}.+?)(\"|\s)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```