#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-enable-success-4722"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4722</EventID>"""
"""<Data Name ='TargetSid'>"""
"""<Data Name ='TargetUserName'>"""
"""<Message>A user account was enabled"""
]
Fields = [
"""SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[^<]+)</Computer>"""
"""({event_code}4722)"""
"""Subject:.+?Account Name:\s*({user}.+?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Target Account:"""
"""Target Account:\s*Security ID:\s*({account_id}.+?)\s*Account Name:\s*({dest_user}.+?)\s*Account Domain:\s*({dest_domain}.+?)\s*<"""
"""({event_name}A user account was enabled)"""
"""<Data Name ='TargetSid'>(?:NONE_MAPPED|({dest_user_sid}[^<]+))<"""
"""<Data Name ='TargetUserName'>({dest_user}[^<]+)<"""
"""<Data Name ='TargetDomainName'>({dest_domain}[^<]+)<"""
"""<Data Name ='SubjectUserSid'>(?:NONE_MAPPED|({user_sid}[^<]+))<"""
"""<Data Name ='SubjectUserName'>({user}[^<]+)<"""
"""<Data Name ='SubjectDomainName'>({domain}[^<]+)<"""
"""<Data Name ='SubjectLogonId'>({login_id}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```