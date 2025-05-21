#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-endpoint-activity-4660
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd HH:mm:ss", "MM/dd/yyyy HH:mm:ss a"]
  Conditions = ["""An object was deleted""", """4660""", """Object Server:""" ]
  Fields = [
    """({event_name}An object was deleted)""",
    """({event_code}4660)""",
    """({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))"""
    """\w{3}\s+\d+\s+\d+:\d+:\d+\s+(\d+|({host}[\w\-\.]+))\s"""
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)[\s,]({host}[\w.-]+)""",
    """<?Computer>?(Name)?\s*=?\s*"*({src_host}({host}[\w\.-]+))(\s|,|"|</Computer>|$)""",
    """Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(am|AM|pm|PM|({host}[\w.\-]+))""",
    """(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """Subject:.+?Security ID:\s*(|-|({user_sid}[^\s]+?))(\s*%\{S-[^\}]+\})*\s*Account Name:\s*(|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s*%\{S-[^\}]+\})*\s*Account Domain:\s*(|-|({domain}.+?))(\s*%\{S-[^\}]+\})*\s*Logon ID:\s*(|-|({login_id}.+?))(\s*%\{S-[^\}]+\})*\s*(Object:|Logon ID:|%\{S-)""",
    """\sObject:.+?Object Server:\s*(|-|({object_server}.+?))(\s*%\{S-[^\}]+\})*\s*Handle ID:\s*(|-|({object_id}.+?))(\s*%\{S-[^\}]+\})*\s*Process Information:\s*(|-|(.+?))(\s*%\{S-[^\}]+\})*\s*Process ID:\s*(|-|({process_id}.+?))(\s*%\{S-[^\}]+\})*\s*Process Name:\s*(|-|({process_path}({process_dir}.*?)({process_name}[^\\\/]+?)))\s*(\w+\s+\w+:|\w+=|%\{S-|\{\w+\-)""", # process_info is removed
  ]
  DupFields = [ "host->dest_host" ]


}
```