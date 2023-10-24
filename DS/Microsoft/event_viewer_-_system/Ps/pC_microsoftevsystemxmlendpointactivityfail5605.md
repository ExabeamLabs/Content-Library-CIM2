#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-activity-fail-5605
  Vendor = Microsoft
  Product = Event Viewer - System
  Conditions = [ """<EventID>5605<""", """<Provider Name ="Microsoft-Windows-WMI"""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """SystemTime\\*="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """Security UserID="({user_sid}[^"\/>]+)""",
    """({event_code}5605)""",
    """<Execution ProcessID="({process_id}\d+)" ThreadID="({thread_id}\d+)"\/>""",
    """<Namespace>({event_hub_namespace}[^<]+)"""
  ]
  ParserVersion = v1.0.0


}
```