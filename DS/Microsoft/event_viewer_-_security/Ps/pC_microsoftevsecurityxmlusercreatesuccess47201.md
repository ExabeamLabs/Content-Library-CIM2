#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-create-success-4720-1"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<EventID>4720</EventID>""",
"""A user account was created"""
  ]
  Fields = [
    """({event_name}A user account was created)""",
    """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[\w\-.]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """Subject:.+?Account Name:\s*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*({src_domain}({domain}.+?))\s*Logon ID:\s*({login_id}.+?)\s*New Account:""",
    """New Account:.+?Security ID:\s*({account_id}.+?)\s*Account Name:\s*({dest_user}({account_name}.+?))\s*Account Domain:\s*({dest_domain}({account_domain}.+?))\s*Attributes"""
    """<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({account_id}[^<]+))</Data>""",
    """<Data Name\\*=('|")TargetUserName('|")>(?=\w)({dest_user}({account_name}[^<]+))</Data>""",
    """<Data Name\\*=('|")TargetDomainName('|")>(?=\w)({dest_domain}({account_domain}[^<]+))</Data>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>""",
    """<Data Name\\*=('|")SubjectUserName('|")>(?=\w)((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>""",
    """<Data Name\\*=('|")SubjectDomainName('|")>(?=\w)({src_domain}({domain}[^<]+))</Data>""",
    """<Data Name\\*=('|")SubjectLogonId('|")>(?=\w)({login_id}[^<]+)</Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```