#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-1108
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>1108<""", """<Provider Name""", """Microsoft-Windows-Eventlog""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """Guid\\*=('|")\{({process_guid}[^\'"\}]+)""",
    """<EventRecordID>({event_id}.+?)<\/EventRecordID>""",
    """<Keywords>({result}[^<]+)""",
    """<EventID>({event_code}\d+)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
	]


}
```