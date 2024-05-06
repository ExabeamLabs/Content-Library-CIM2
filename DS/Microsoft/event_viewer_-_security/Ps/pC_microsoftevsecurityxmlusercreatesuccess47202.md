#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-create-success-4720-2"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """<EventID>4720</EventID>""","""<Data Name""","""TargetSid""","""<Message>A user account was created"""
  ]
  Fields = [
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""<Computer>({host}[\w\-.]+)<""",
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""({event_code}4720)""",
"""<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({account_id}[^<]+))<""",
"""<Data Name\\*=('|")TargetUserName('|")>({account_name}[^<]+)<""",
"""<Data Name\\*=('|")TargetDomainName('|")>({account_domain}[^<]+)<""",
"""<Data Name\\*=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))<""",
"""<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-]{1,40}\$?))<""",
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)<""",
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<""",
"""({event_name}A user account was created)"""
"""<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "account_name->dest_user" ]


}
```