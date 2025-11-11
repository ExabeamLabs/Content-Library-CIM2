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
    """Security ID:\s*(SYSTEM|({dest_user_sid}({user_sid}\S+)))\s+Account Name:""",
    """Account Name:\s*(SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:""",
    """Account Domain:\s*({dest_domain}({domain}\S+))\s+Logon ID:""",
    """"+LogonType"+:"+({login_type}\d+)"+""",
    """"+TargetUserName"+:"+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+""",
    """"+TargetLogonId"+:"+({dest_login_id}({login_id}[^"]+))"+""",
    """"+TargetDomainName"+:"+({dest_domain}({domain}[^"]+))"+""",
    """"+TargetUserSid"+:"+({dest_user_sid}({user_sid}[^"]+))"+"""
  ]


}
```