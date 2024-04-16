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
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Task>({task_name}[^<]+)""",
    """<Data Name\\*='LocalAddress'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Data Name\\*='LocalKeyModPort'>({src_port}\d+)""",
    """<Data Name\\*='RemoteAddress'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name\\*='RemoteKeyModPort'>({dest_port}\d+)""",
    """<Data Name\\*='FailureReason'>({failure_reason}[^<]+)"""
# em_auth_method is removed
    """<Data Name\\*='State'>({state}[^<]+)""",
    """<Data Name\\*='Role'>({role}[^<]+)""",
    """<Keywords>({action}[^<]+)""",
    """<Level>({run_level}[^<]+)<"""
    ]


}
```