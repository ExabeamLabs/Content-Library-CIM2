#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-session-fail-4984
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4984<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Execution ProcessID='({process_id}\d+)""",
    """<Task>({task_name}[^<]+)""",
    """<Data Name ='LocalAddress'>({src_ip}[^<]+)""",
    """<Data Name ='LocalKeyModPort'>({src_port}\d+)""",
    """<Data Name ='RemoteAddress'>({dest_ip}[^<]+)""",
    """<Data Name ='RemoteKeyModPort'>({dest_port}\d+)""",
    """<Data Name ='FailureReason'>({failure_reason}[^<]+)"""
# em_auth_method is removed
    """<Data Name ='State'>({state}[^<]+)""",
    """<Data Name ='Role'>({role}[^<]+)""",
    """<Keywords>({action}[^<]+)"""
    ]


}
```