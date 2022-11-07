#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-4655
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4655<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Execution ProcessID='({process_id}\d+)""",
    """<Task>({task_name}[^<]+)""",
    """<Data Name ='LocalAddress'>({src_ip}[^<]+)""",
    """<Data Name ='RemoteAddress'>({dest_ip}[^<]+)""",
    """<Keywords>({result}[^<]+)"""
    ]


}
```