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
"""SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[^<]+)</Computer>"""
"""<EventID>({event_code}[^<]+)</EventID>"""
"""Subject:.+?Security ID:\s*({user_sid}.+?)\s*Account Name:"""
"""Subject:.+?Account Name:\s*({user}[^:]+?)\s*Account Domain:\s*(|({domain}[^:]+?))\s*Logon ID"""
"""Logon ID:\s*({login_id}.+?)\s*Target Account:"""
"""Target Account:\s*Security ID:\s*({dest_user_sid}.+?)\s*Account Name:\s*(?=\w)({dest_user}.+?)\s*Account Domain"""
"""Target Account.+?Account Domain:\s*(?=\w)({dest_domain}.+?)\s*</EventData>"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```