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
    """<Data Name(\\)?='SourceAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Data Name(\\)?='SourcePort'>({src_port}\d+)"""
    """<Data Name(\\)?='DestAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name(\\)?='DestPort'>({dest_port}\d+)""",
    """<Data Name(\\)?='Protocol'>({protocol}[^<]+)"""
    """({event_name}The Windows Filtering Platform has blocked a packet)"""
    ]


}
```