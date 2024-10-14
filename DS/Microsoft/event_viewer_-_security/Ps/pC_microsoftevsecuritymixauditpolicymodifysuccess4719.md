#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-audit-policy-modify-success-4719"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
Conditions = [
"""4719"""
"""System audit policy was changed"""
]
Fields = [
"""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""TimeCreated":"[\\\/]*Date\(({time}\d{13})"""
"""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
"""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
"""({event_name}System audit policy was changed)"""
""""computer":"({src_host}({host}[\w\-.]+))"""
"""({host}[\w\-.]+)\sMSWinEventLog"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""({event_code}4719)"""
"""\s+Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain"""
"""\s+Account Domain:\s+({domain}[^\s]+)"""
"""\s+Logon ID:\s+({login_id}[^\s]+)"""
"""\s+Category:\s+({audit_category}.+?)\s+Subcategory:"""
"""\s+Subcategory:\s+({sub_category}.+?)\s+Subcategory GUID:"""
"""\s+Changes:\s+({audit_policy_name}.*?)\s*(\||\d|<|\",)"""
]
ParserVersion = "v1.0.0"


}
```