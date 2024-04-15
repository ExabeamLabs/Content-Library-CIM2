#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-fail-lockedout"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""EventCode=4740"""
"""EventType="""
"""A user account was locked out"""
]
Fields = [
"""({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))"""
"""ComputerName =({dest_host}[\w\-.]+)"""
"""({event_code}4740)"""
"""({event_name}A user account was locked out)"""
"""RecordNumber=({event_id}[^;\"]+)"""
"""Keywords=({result}[^;\"]+)"""
"""Subject=.*?Account Name =({src_user}[^;\"\s]+)"""
"""Subject=.*?Account Domain=({src_domain}[^;\"\s]+)"""
"""Logon ID=({login_id}[^;\"\s]+)"""
"""Security ID=({user_sid}[^;\"]+);Account Name =({user}[^;\"\s]+);Additional Information="""
"""Caller Computer Name =\\*({src_host}[\w\-.]+)"""
]
DupFields = [
"src_domain->domain"
]
ParserVersion = "v1.0.0"


}
```