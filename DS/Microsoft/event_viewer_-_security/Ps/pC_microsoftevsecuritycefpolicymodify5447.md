#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-policy-modify-5447
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """5447""", """A Windows Filtering Platform filter has been changed""" ]
  Fields = [
    """({event_name}A Windows Filtering Platform filter has been changed)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """({event_code}5447)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)""",
    """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s""",
    """Subject:.+?Security ID:\s*({user_sid}[^\s]+)""",
    """Subject:.+?Account Name:\s*((NT AUTHORITY|({domain}[^\\\s]+))\\+)?(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Process Information:""",
# change_type is removed
# filter_id is removed
# filter_name is removed
  ]


}
```