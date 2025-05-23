#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-modify-4717
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Conditions = [ """4717""", """System security access was granted to an account""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """"Computer":"({host}[\w\-\.]+)"""",
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
    """({event_code}4717)""",
    """({event_name}System security access was granted to an account)""",
    """Subject:.*?Security ID:\s*(|({user_sid}.+?))\s*Account Name:\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|({domain}.+?))\s*Logon ID:\s*(|({login_id}.+?))\s*Account Modified:""",
    """Account Modified:.*?Account Name:\s*(|(({dest_domain}\S[^\\\/]*?)?[\\\/]+)?(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_sid}[^\s]+)))\s*Access Granted:""",
    """Access Granted:.*?Access Right:\s*({access_type}.+?)\s*("|<|$)"""
  ]
}, 

${WindowsParsersTemplates.windows-defender-1}{
  Name = microsoft-defenderep-kv-endpoint-scan-updated
  ParserVersion = v1.0.0
  Product = Microsoft Defender
  Conditions = [ """Microsoft-Windows-Windows Defender/Operational""", """Windows Defender signature version has been updated"""]
  Fields = ${WindowsParsersTemplates.windows-defender-1.Fields}[
    """({event_name}Windows Defender signature version has been updated)"""
    ]


}
```