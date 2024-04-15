#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-fail-accountname"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Account That Was Locked Out"""
""" ComputerName ="""
"""Account Name ="""
""" EventID=4740 """
]
Fields = [
"""({event_name}Account That Was Locked Out)"""
"""({event_code}4740)"""
"""\sComputerName =({host}[^\s]+)"""
"""Locked Out:Security ID=({user_sid}[^\s]+)"""
"""\sDetectTime=({time}\d\d\d\d-\d+-\d+ \d+:\d+:\d+)\s"""
"""\sUser=(null|({user}[^\s]+))"""
"""\sEventType=({result}[^\s]+)"""
"""Caller Computer Name =({src_host}[^\s]+)"""
"""Account Name =({user}[^\s]+)"""
"""Account Domain=({domain}[^\s]+)"""
"""Logon ID=({login_id}[^\s\"]+)"""
"""Security ID=({user_id}[^\s]+)"""
]
DupFields = [
"host->dest_host"
"user_domain->src_domain"
]
ParserVersion = "v1.0.0"


}
```