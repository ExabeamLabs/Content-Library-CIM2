#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-logout-success-7002
  ParserVersion = v1.0.0
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Product = Event Viewer - System
  Conditions = [ """<EventID>7002<""", """<Provider Name""","""Microsoft-Windows-Winlogon""","""<Channel>System</Channel>"""]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[\w\-.]+)<""",
    """Guid\\*=('|")\{({process_guid}[^\'\"\}]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """<EventID[^<]*?>({event_code}\d+)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name\\*=('|")({provider_name}[^\'\"]+)""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>"""
    """<Level>({run_level}[^<]+)<"""
 ]


}
```