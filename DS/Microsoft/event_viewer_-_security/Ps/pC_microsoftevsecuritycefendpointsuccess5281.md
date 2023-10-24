#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-success-528-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""MSWinEventLog"""
""",528,"""
"""Security"""
"""Successful Logon:"""
"""rsa_sa_log"""
]
Fields = [
"""({event_name}Successful Logon)"""
"""(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+),"""
"""\d{2}:\d{2}:\d{2} \d{4

}
```