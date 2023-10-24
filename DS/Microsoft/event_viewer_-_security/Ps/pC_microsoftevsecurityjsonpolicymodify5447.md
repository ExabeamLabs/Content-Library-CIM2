#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-policy-modify-5447
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"EventID":5447,""", """A Windows Filtering Platform filter has been changed""" ]
  Fields = [
    """({event_name}A Windows Filtering Platform filter has been changed)""",
    """({event_code}5447)""",
    """"EventTime"+:\s*"+({time}[^",]+)""",
    """"Hostname"+:"+({host}[^",]+)""",
    """"UserSid"+:"+({user_sid}[^",]+)""",
# filter_id is removed
# filter_name is removed
# filter_type is removed
    """"UserName"+:"+((NT AUTHORITY|({domain}[^\\\s]+))\\+)?(LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))""",
# change_type is removed
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  ]


}
```