#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-modify-success-4737
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "EEE MMM dd HH:mm:ss yyyy","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","MM/dd/yyyy HH:mm:ss a" ]
  ParserVersion = "v1.0.0"
  Conditions = [ """A security-enabled global group was changed""", """4737""", """Security Group Management""", """Group:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """({time}\w{3}\s\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+\d+\s+""",
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))""",
    """({event_name}A security-enabled global group was changed)""",
    """<Computer>({host}[\w\-.]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({event_code}4737)""",
    """Subject:[\s\S]*?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*Group:\s*(|-|({group_name}.+?))\s*Security ID:\s*(|-|({group_id}.+?))\s*Group Name:\s*(|-|({=group_name}.+?))\s+(Group Domain:\s*(|-|({group_domain}.+?))\s*Changed Attributes:\s*(|-|(.+?))\s*SAM Account Name:\s*(|-|(.+?))\s*SID History:\s*(|-|({sid_history}.+?))\s*)?(Additional Information:\s*(|-|({additional_info}.+?))\s*Privileges:\s*(|-|({privileges}.+?))(\s*|\s+\d+\s*)($|<))?"""
# DL Fields are removed
  ]


}
```