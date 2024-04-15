#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-disable-success-4725"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""A user account was disabled"""
]
Fields = [
"""({event_name}A user account was disabled)"""
"""SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""Security(,|\s+)({event_id}[\d]+)"""
"""({event_code}4725)"""
"""(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)({host}[^,\s\=]+)"""
"""Information\s+({host}[\w.\-]+)\s+"""
"""({host}[^\/\s]+)\/Microsoft-Windows-Security-Auditing"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}.+?)(\"|\s)"""
"""\"system_name\":\"({host}[^\"]+)\""""
"""Subject:.+?Security ID:\s+({user_sid}.+?)(\\[nrt]\s+|\s+)Account Name:"""
"""Subject:.+?Account Name:\s+({user}.+?)(\\[nrt]\s+|\s+)Account Domain:\s+({domain}.+?)(\\[nrt]\s+|\s+)Logon ID"""
"""Logon ID:\s+({login_id}.+?)(\s|\\[nrt])"""
"""Target Account.+?Security ID:\s*(%\{)?({dest_user_sid}.+?)\}?(\\[nrt]\s+|\s+)Account Name:\s+({dest_user}.+?)(\\[nrt]\s+|\s+)Account Domain"""
"""Target Account.+?Account Domain:\s*(?=\w)(({dest_domain}[^\s\^\r\n$\",]+)|)(\s+[^\^\r\n$])?"""
"""\"SubjectUserSid\":\"({user_sid}[^\"]+)"""
"""\"SubjectDomainName\":\"({domain}[^\"]+)"""
"""\"SubjectLogonId\":\"({login_id}[^\"]+)"""
"""\"SubjectUserName\":\"({user}[^\"]+)"""
"""\"TargetSid\":\"({dest_user_sid}[^\"]+)"""
"""\"TargetDomainName\":\"({dest_domain}[^\"]+)"""
"""\"TargetUserName\":\"({dest_user}[^\"]+)"""
"""<Data Name ='SubjectUserSid'>(?:NONE_MAPPED|({user_sid}[^<]+))<"""
"""<Data Name ='SubjectDomainName'>({domain}[^<]+)<"""
"""<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"""
"""<Data Name ='SubjectUserName'>({user}[^<]+)<"""
"""<Data Name ='TargetSid'>(?:NONE_MAPPED|({dest_user_sid}[^<]+))<"""
"""<Data Name ='TargetDomainName'>({dest_domain}[^<]+)<"""
"""<Data Name ='TargetUserName'>({dest_user}[^<]+)<"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```