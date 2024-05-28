#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-logout-success-4634-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":4634,""", """An account was logged off""", """SourceModuleName""", """SourceModuleType""", """TargetLogonId""", """TargetUserSid""" ]
  Fields = [
    """"+EventTime"+:"+({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"+""",
    """"+Hostname"+:"+({host}[^"]+)"+""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+""",
    """({event_code}4634)""",
    """({event_name}An account was logged off)""",
    """Security ID:\s*(SYSTEM|({user_sid}\S+))\s+Account Name:""",
    """Account Name:\s*(SYSTEM|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """"+LogonType"+:"+({login_type}\d+)"+""",
    """"+TargetUserName"+:"+({user}[\w\.\-]{1,40}\$?)"+""",
    """"+TargetLogonId"+:"+({login_id}[^"]+)"+""",
    """"+TargetDomainName"+:"+({domain}[^"]+)"+""",
    """"+TargetUserSid"+:"+({user_sid}[^"]+)"+""",
  ]


}
```