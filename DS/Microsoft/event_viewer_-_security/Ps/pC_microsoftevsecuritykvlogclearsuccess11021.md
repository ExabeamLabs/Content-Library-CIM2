#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-log-clear-success-1102-1"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = ["""     1102    ""","""The audit log was cleared"""]
Fields = [
"""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
"""Hostname":"({host}[\w\-.]+)""""
"""({event_code}1102)"""
"""({event_name}The audit log was cleared)"""
"""\s+Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Domain"""
"""\s+Domain Name:\s+({domain}[^\s]+)"""
"""\s+Logon ID:\s+({login_id}[^\s]+)"""
"""\s+(Information|Audit Success|Success Audit)\s+({host}[\w.\-]+)"""
"""\s+(Information|Audit Success|Success Audit)\s+(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))"""
"""\s+({time}\w+\s+\d+\s+\d\d:\d\d:\d\d\s+\d\d\d\d)\s+"""
]
DupFields = [ "host->src_host" ]


}
```