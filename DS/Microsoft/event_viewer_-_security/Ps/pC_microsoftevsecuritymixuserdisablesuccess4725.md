#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-disable-success-4725"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [
"""A user account was disabled"""
]
Fields = [
"""({event_name}A user account was disabled)"""
"""TimeGenerated=({time}\d{10})"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""Security(,|\s+)({event_id}[\d]+)"""
"""({event_code}4725)"""
"""(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)({host}[^,\s\=]+)"""
"""Information\s+({host}[\w.\-]+)\s+"""
"""({host}[^\/\s]+)\/Microsoft-Windows-Security-Auditing"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}[\w\-.]+?)(\"|\s)"""
"""\"system_name\":\"({host}[\w\-.]+)\""""
"""Subject:.+?Security ID:\s+({user_sid}S-.+?)(\\[nrt]\s+|\s+)Account Name:"""
"""Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\[nrt]\s+|\s+)Account Domain:\s+({domain}.+?)(\\[nrt]\s+|\s+)Logon ID"""
"""Logon ID:(\s|\\[nrt])*({login_id}.+?)(\s|\\[nrt])"""
"""Target Account.+?Security ID:\s*(%\{)?(\\t|\\r|\\n|\s)*({dest_user_sid}S-[^\s]+?)\}?(\\t|\\r|\\n|\s)*Account Name:""",
"""Target Account.+?Account Name:(\\t|\\r|\\n|\s)*({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\s)*Account Domain""",
"""Target Account.+?Account Domain:(\\t|\\r|\\n|\s)*(({dest_domain}[^\t\s\^\r\n$\",]+)|)(\s+[^\t\r\n$])?"""
"""\"SubjectUserSid\":\"({user_sid}S-[^\"]+)"""
"""\"SubjectDomainName\":\"({domain}[^\"]+)"""
"""\"SubjectLogonId\":\"({login_id}[^\"]+)"""
"""\"SubjectUserName\":\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\"TargetSid\":\"({dest_user_sid}S-[^\"]+)?"""
"""\"TargetDomainName\":\"({dest_domain}[^\"]+)"""
"""\"TargetUserName\":\"({dest_user}[^\"]+)"""
"""<Data Name\\*='SubjectUserSid'>(?:NONE_MAPPED|({user_sid}S-[^<]+))<"""
"""<Data Name\\*='SubjectDomainName'>({domain}[^<]+)<"""
"""<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)<"""
"""<Data Name\\*='SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
"""<Data Name\\*='TargetSid'>(?:NONE_MAPPED|({dest_user_sid}S-[^<]+))<"""
"""<Data Name\\*='TargetDomainName'>({dest_domain}[^<]+)<"""
"""<Data Name\\*='TargetUserName'>({dest_user}[^<]+)<"""
"""Target Account.+?Account Name:\s*(\\t)?({dest_user}[^:].+?)\s*(\\n|\\r\s\\t)*?\s*Account Domain:\s*(\\t)?({dest_domain}[^:]+?)\s+"""
"""Target Account.+?Account Domain:\s*(?=\w)(({dest_domain}[^\s\^\r\n$\",]+)|)(\s+[^\^\r\n$])?"""
"""Logon ID:\s+(\\t)?({login_id}.+?)\s*(\\n|\\r\s\\r\s\\n)*?Target Account:"""
]
ParserVersion = "v1.0.0"


}
```