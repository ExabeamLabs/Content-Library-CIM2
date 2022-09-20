#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-traffic-fail-5152
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>5152<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Execution ProcessID(\\)?='({process_id}\d+)""",
    """<Task>({task_name}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Data Name(\\)?='SourceAddress'>({src_ip}[^<]+)""",
    """<Data Name(\\)?='SourcePort'>({src_port}\d+)"""
    """<Data Name(\\)?='DestAddress'>({dest_ip}[^<]+)""",
    """<Data Name(\\)?='DestPort'>({dest_port}\d+)""",
    """<Data Name(\\)?='Protocol'>({protocol}[^<]+)"""
    ]


}
```