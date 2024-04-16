#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-disable-success-629
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MMM dd HH:mm:ss yyyy","epoch_sec"]
Conditions = [
"""User Account Disabled"""
"""629"""
]
Fields = [
"""({event_name}User Account Disabled)"""
"""\sTimeGenerated=({time}\d{10})"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+({event_code}629)\s+Security\s.+?(?i)((audit|success)( |_)(success|audit))\s+({host}[\w\-.]+)"""
"""\srt=({time}\d{13})""",
"""({host}[\w\-.]+)\/Security"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}[\w\-.]+?)(\"|\s)"""
"""({event_code}629)"""
"""Target Account Name:\s+({dest_user}.+?)\s+Target Domain:\s+({dest_domain}.+?)\s+Target Account ID:.*?({dest_user_sid}[\w\-\d]+)\}?\s+Caller User Name"""
"""Caller User Name:\s+(?=\w)({user}[\w\.\-]{1,40}\$?)\s+Caller Domain:\s+(?=\w)({domain}.+?)\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```