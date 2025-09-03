#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-disable-success-4725"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4725</EventID>"""
"""A user account was disabled"""
]
Fields = [
"""({event_name}A user account was disabled)"""
"""SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[\w\-.]+)</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<EventID>({event_code}[^<]+)</EventID>"""
"""Subject:.+?Security ID:\s*({user_sid}.+?)\s*Account Name:"""
"""Subject:.+?Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*(|({domain}[^:]+?))\s*Logon ID"""
"""Logon ID:\s*({login_id}.+?)\s*Target Account:"""
"""Target Account:\s*Security ID:\s*({dest_user_sid}.+?)\s*Account Name:\s*(?=\w)({dest_user}.+?)\s*Account Domain"""
"""Target Account.+?Account Domain:\s*(?=\w)({dest_domain}.+?)\s*</EventData>"""
]
ParserVersion = "v1.0.0"


}
```