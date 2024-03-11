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
    """<Data Name ='LocalAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Data Name ='LocalKeyModPort'>({src_port}\d+)""",
    """<Data Name ='RemoteAddress'>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name ='RemoteKeyModPort'>({dest_port}\d+)""",
    """<Data Name ='MMLifetime'>({duration}[^<]+)""",
    """<Keywords>({action}[^<]+)"""
    ]


}
```