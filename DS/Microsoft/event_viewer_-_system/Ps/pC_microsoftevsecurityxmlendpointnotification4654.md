#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4654
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4654<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Data Name\\*='LocalAddress'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
# subnet_mask is removed
    """<Data Name\\*='LocalPort'>({src_port}\d+)""",
    """<Data Name\\*='LocalTunnelEndpoint'>({src_translated_ip}[^<]+)""",
    """<Data Name\\*='RemoteAddress'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name\\*='RemotePort'>({dest_port}\d+)""",
    """<Data Name\\*='RemoteTunnelEndpoint'>({dest_translated_ip}[^<]+)""",
    """<Data Name\\*='FailureReason'>({failure_reason}[^<]+)""",
    """<Task>({task_name}[^<]+)""",
    """<Keywords>({result}[^<]+)"""
    ]


}
```