#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-5451
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>5451<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Execution ProcessID='({process_id}\d+)""",
    """<Task>({task_name}[^<]+)""",
    """<Keywords>({result}[^<]+)"""
    """<Data Name ='LocalAddress'>({src_ip}[^<]+)""",
    """<Data Name ='RemoteAddress'>(-|({dest_ip}[^<]+))""",
    """<Data Name ='LocalPort'>({src_port}\d+)""",
    """<Data Name ='LocalTunnelEndpoint'>({src_translated_ip}[^<]+)""",
    """<Data Name ='RemotePort'>({dest_port}\d+)""",
    """<Data Name ='RemoteTunnelEndpoint'>({dest_translated_ip}[^<]+)""",
    """<Data Name ='LifetimeSeconds'>({duration}[^<]+)"""
    """<Data Name ='Role'>({role}[^<]+)""",
# mode is removed
    ]


}
```