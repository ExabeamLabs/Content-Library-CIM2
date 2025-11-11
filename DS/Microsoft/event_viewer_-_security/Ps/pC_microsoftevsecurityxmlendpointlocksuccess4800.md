#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-lock-success-4800"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
Conditions = [
"""<EventID>4800"""
"""TargetUserName"""
]
Fields = [
  """<EventTime>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
"""<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)"""
"""<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
"""<Computer>({dest_host}({host}[\w\-.]+))"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""({event_name}The workstation was locked)"""
"""({event_code}4800)"""
"""Data Name(\\)?=('|")TargetUserName('|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""Data Name(\\)?=('|")TargetDomainName('|")>({dest_domain}({domain}[^<]+))"""
"""Data Name(\\)?=('|")TargetLogonId('|")>({dest_login_id}({login_id}[^<]+))"""
"""Data Name(\\)?=('|")TargetUserSid('|")>({dest_user_sid}({user_sid}[^<]+))"""
"""<Hostname>({dest_host}({host}[^\.\<]+))\.({dest_domain}({domain}[^\s\<]+))<"""
"""<ProcessID>({process_id}\d+)<"""
"""<Category>({category}[^\<]+)<"""
"""<Severity>({alert_severity}[^\<]+)<""",
"""<TargetLogonId>({dest_login_id}({login_id}[^\<]+))<""",
"""<TargetUserName>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
"""<TargetDomainName>({dest_domain}[^\<]+)<""",
"""<RecordNumber>({event_id}\d+)<""",
"""<TargetUserSid>({dest_user_sid}({user_sid}[^\<]+))<""",
"""<Level>({run_level}[^<]+)"""
]
ParserVersion = "v1.0.0"


}
```