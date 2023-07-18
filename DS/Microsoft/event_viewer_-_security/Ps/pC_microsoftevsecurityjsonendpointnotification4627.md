#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-notification-4627
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"EventID":4627,""", """Group membership information""" ]
  Fields = [
    """({event_name}Group membership information)""",
    """({event_code}4627)""",
    """"Hostname"+:"+({host}[^",]+)""",
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"SubjectUserSid"+:"+(SYSTEM|NT AUTHORITY|\\NULL SID|({user_sid}[^"]+))""",
    """"SubjectUserName"+:"+(-|({account_name}[^"]+))""",
    """"SubjectDomainName"+:"+(-|({account_domain}[^"]+))""",
    """"SubjectLogonId"+:"+({login_id}[^"]+)""",
    """"TargetUserSid"+:"+(SYSTEM|ANONYMOUS|({user_sid}[^",]+))""",
    """"TargetUserName"+:"+(SYSTEM|ANONYMOUS|({user}[^"]+))""",
    """"TargetDomainName"+:"+(NT AUTHORITY|({domain}[^"]+))""",
    """"TargetLogonId"+:"+({login_id}[^"]+)""",
    """"LogonType"+:"+({login_type}\d+)""",
# sequence_num is removed
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  ]


}
```