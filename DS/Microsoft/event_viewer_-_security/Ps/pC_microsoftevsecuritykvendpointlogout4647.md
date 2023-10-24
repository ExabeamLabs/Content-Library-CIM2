#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-logout-4647
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd HH:mm:ss"]
  Conditions = ["""User initiated logoff""", """4647"""]
  Fields = [
    """({event_name}User initiated logoff)""",
    """({event_code}4647)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z)""",
    """\s(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)[\s,]({host}[\w.-]+)""",
    """<?Computer>?(Name)?\s*=?\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({host}[\w.\-]+))""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}[\w\.\-]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}\S+))\s""",
    """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """"TargetLogonId":"({login_id}[^\\\s"]+)""",
    """"TargetUserSid":"({user_sid}[^\\\s"]+)""",
    """\WdestinationServiceName =({app}.+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```