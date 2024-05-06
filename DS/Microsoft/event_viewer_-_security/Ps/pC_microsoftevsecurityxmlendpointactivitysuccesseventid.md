#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-success-eventid
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>""", """<Computer>""", """<Provider Name =""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """Guid\\*=('|")\{({process_guid}[^\'"\}]+)""",
    """<EventRecordID>({event_id}.+?)<\/EventRecordID>""",
    """<Keywords>({result}[^<]+)""",
    """<EventID>({event_code}\d+)""",
    """<Computer>({host}[\w\-.]+)""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
    """<Data Name\\*=('|")ErrorCode('|")>({error_code}\d+)<\/Data>""",
    ]


}
```