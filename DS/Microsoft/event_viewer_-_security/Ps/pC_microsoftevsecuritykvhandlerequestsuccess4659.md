#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-request-success-4659
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""A handle to an object was requested with intent to delete""", """4659"""]
  Fields = [
    """({event_name}A handle to an object was requested with intent to delete)""",
    """({event_code}4659)""",
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)[\s,]({host}[\w.-]+)""",
    """<?Computer>?(Name)?\s*=?\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({host}[\w.\-]+))""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}[\w\.\-]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*Object:""",
    """\sObject:.+?Object Server:\s*(|-|({object_server}.+?))\s*Object Type:\s*(|-|({object_type}.+?))\s*Object Name:\s*(|-|({object}.+?))\s*Handle ID:\s*(|-|({object_id}.+?))\s*Process Information:\s*(|-|(.+?))\s*Process ID:\s*(|-|({process_id}.+?))\s*Access Request Information:""", # process_info is removed
  ]
  DupFields = [ "host->dest_host" ]


}
```