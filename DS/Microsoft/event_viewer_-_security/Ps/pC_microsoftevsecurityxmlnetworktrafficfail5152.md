#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-traffic-fail-5152
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [ """<EventID>5152<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID(\\)?='({process_id}\d+)""",
    """<Task>({task_name}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Data Name(\\)?='SourceAddress'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Data Name(\\)?='SourcePort'>({src_port}\d+)"""
    """<Data Name(\\)?='DestAddress'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name(\\)?='DestPort'>({dest_port}\d+)""",
    """<Data Name(\\)?='Protocol'>({protocol}[^<]+)""",
    """({event_name}The Windows Filtering Platform has blocked a packet)""",
    """Direction:[\s\S]*?({direction}[^\s]+)""",
    """<Data Name(\\)?='Application'>(-|({process_path}({process_dir}([^<]+)?[\\\/])?({process_name}[^\\\/]+?)))<"""
    """<Data Name\\*='Direction'>({direction}(Inbound|Outbound))</Data>"""
    """<Message>({failure_reason}.+?)\s*(:|\.)"""
    """Direction:((?-i)\\+[rnt])*\s*({direction}Outbound|Inbound)"""
    """<Computer>({dest_host}[\w\-.]+)</Computer>"""
    """<Level>({run_level}[^<]+)<"""
    ]


}
```