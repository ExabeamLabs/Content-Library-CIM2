#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-policy-modify-5447
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>5447<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}\d+)""",
    """<Task>({task_name}[^<]+)""",
    """<Data Name(\\)?=('|")UserSid('|")>({user_sid}[^<]+)""",
# provider_key is removed
    """<Data Name(\\)?=('|")UserName('|")>(((?i)NT AUTHORITY|(({domain}[^\\]+)))\\)?((?i)LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """<Data Name(\\)?=('|")ProviderName('|")>({provider_name}[^<]+)""",
    """<Data Name(\\)?=('|")ChangeType('|")>({event_category}[^<]+)""",
# filter_key is removed
# filter_name is removed
    """<Data Name(\\)?=('|")Action('|")>({action}[^<]+)""",
    """<Keywords>({result}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
    ]


}
```