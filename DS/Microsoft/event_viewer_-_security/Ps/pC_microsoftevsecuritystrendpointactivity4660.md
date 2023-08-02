#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-endpoint-activity-4660
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""An object was deleted""", """4660"""]
  Fields = [
    """({event_name}An object was deleted)""",
    """({event_code}4660)""",
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)[\s,]({host}[\w.-]+)""",
    """<?Computer>?(Name)?\s*=?\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({host}[\w.\-]+))""",
    """(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}.+?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*Object:""",
    """\sObject:.+?Object Server:\s*(|-|({object_server}.+?))\s*Handle ID:\s*(|-|({object_id}.+?))\s*Process Information:\s*(|-|(.+?))\s*Process ID:\s*(|-|({process_id}.+?))\s*Process Name:\s*(|-|({process_path}({process_dir}.*?)({process_name}[^\\\/]+?)))\s*Transaction ID:""", # process_info is removed
  ]
  DupFields = [ "host->dest_host" ]


}
```