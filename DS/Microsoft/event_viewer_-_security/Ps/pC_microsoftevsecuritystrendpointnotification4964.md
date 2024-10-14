#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-endpoint-notification-4964
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """4964""", """Special groups have been assigned to a new logon""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(Z|(\+|\-)\d\d:\d\d))\s+({host}[\w.\-]+)""",
    """({event_code}4964)""",
    """({event_name}Special groups have been assigned to a new logon)""",
    """Subject:.*?Security ID:\s*(|({user_sid}.+?))\s*Account Name:\s*(|({account_name}.+?))\s*Account Domain:\s*(|({account_domain}.+?))\s*Logon ID:\s*({login_id}\S+)\s*Logon GUID:\s*({session_id}\S+)""",
    """New Logon:.*?Security ID:\s*(|({user_sid}.+?))\s*Account Name:\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|({domain}.+?))\s*Logon ID:\s*({login_id}\S+)\s*Logon GUID:\s*({logon_guid}\S+)""",
    """Special Groups Assigned:\s*({group_info}.+?\})\s*"""
  ]


}
```