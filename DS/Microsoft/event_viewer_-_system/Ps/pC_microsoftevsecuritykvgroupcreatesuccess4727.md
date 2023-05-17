#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-create-success-4727
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  ParserVersion = "v1.0.0"
  Conditions = [ """A security-enabled global group was created""", """4727""" ]
  Fields = [
    """({event_name}A security-enabled global group was created)""",
    """<Computer>({dest_host}({host}[^<]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({event_code}4727)""",
    """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}.+?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*Group:\s*(|-|({group_name}.+?))\s*Security ID:\s*(|-|({group_id}.+?))\s*Group Name:\s*(|-|({=group_name}.+?))\s*Group Domain:\s*(|-|({group_domain}.+?))\s*""",
    """Group Domain:\s+({group_domain}[\w]+)\s+""",
    """SAM Account Name:\s*(|-|(.+?))\s*SID History:\s*(|-|({sid_history}.+?))\s*Additional Information:\s*(|-|({additional_info}.+?))\s*Privileges:\s*(|-|({privileges}.+?))(\s*|\s+\d+\s*)($|<)"""
# DL Fields are removed
]


}
```