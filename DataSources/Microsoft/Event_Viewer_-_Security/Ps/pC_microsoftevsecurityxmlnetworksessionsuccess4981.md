#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-session-success-4981
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4981<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Execution ProcessID='({process_id}\d+)""",
    """<Task>({task_name}[^<]+)""",
    """<Data Name ='LocalMMPrincipalName'>({src_host}[^<]+)""",
# local_hash is removed
# local_mm_issue_ca is removed
# local_mm_root_ca is removed
    """<Data Name ='RemoteMMPrincipalName'>({dest_host}[^<]+)""",
# remote_hash is removed
# remote_mm_issue_ca is removed
# remote_mm_root_ca is removed
    """<Data Name ='LocalAddress'>({src_ip}[^<]+)""",
    """<Data Name ='LocalKeyModPort'>({src_port}\d+)""",
    """<Data Name ='RemoteAddress'>({dest_ip}[^<]+)""",
    """<Data Name ='RemoteKeyModPort'>({dest_port}\d+)""",
    """<Data Name ='MMLifetime'>({duration}[^<]+)""",
    """<Keywords>({action}[^<]+)"""
    ]


}
```