#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-unlock-success-4767-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
Conditions = [
"""<EventID>4767</EventID>"""
"""A user account was unlocked"""
]
Fields = [
"""({event_name}A user account was unlocked)"""
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
"""<Computer>({host}[\w\-.]+)</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<EventID>({event_code}\d+)</EventID>"""
"""Subject:[\s\S]*?Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Target Account:"""
"""Target Account:\s*Security ID:\s*({user_sid}.+?)\s*Account Name:\s*({dest_user}.+?)\s*Account Domain:\s*({dest_domain}[^=<]+)\s*<"""
"""<Data Name\\*=('|")SubjectLogonId('|")>\s*({login_id}.+?)\s*</Data>"""
"""<Data Name\\*=('|")SubjectUserSid('|")>\s*({user_sid}[^\s]+?)\s*</Data>"""
"""<Data Name\\*=('|")TargetSid('|")>\s*({dest_user_sid}.+?)</Data>\s*"""
"""<Data Name ='SubjectUserName'>\s*(SYSTEM|({user}[\w\.\-]{1,40}\$?))\s*</Data>"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```