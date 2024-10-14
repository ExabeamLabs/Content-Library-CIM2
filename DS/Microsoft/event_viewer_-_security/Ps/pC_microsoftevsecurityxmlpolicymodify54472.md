#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-policy-modify-5447-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>5447</EventID>""", """<Task>Other Policy Change Events""", """A Windows Filtering Platform filter has been changed""" ]
  Fields = [
    """({event_name}A Windows Filtering Platform filter has been changed)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z('|")\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """Subject:.+?Security ID:\s*({user_sid}[^\s]+)""",
    """Subject:.+?Account Name:\s*((NT AUTHORITY|({domain}[^\\\s]+))\\+)?(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """<Level>({run_level}[^<]+)<"""
# change_type is removed
# filter_id is removed
# filter_name is removed
  ]


}
```