#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-create-success-4720"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<EventID>4720</EventID>""",
"""TargetSid""",
"""<Data Name""",
"""</Data>"""
  ]
  Fields = [
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""<Computer>({src_host}({host}[\w\-.]+))</Computer>""",
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))""",
"""<EventID>({event_code}[^<]+)</EventID>""",
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