#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-network-session-fail-5157"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [ """<EventID>5157</EventID>""", """<Event xmlns""" ]
  Fields = [
    """({event_name}The Windows Filtering Platform has blocked a connection)""",
    """<TimeCreated SystemTime(\\)?=['"]+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z['"]+/>""",
    """<TimeCreated SystemTime(\\)?=['"]+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)['"]+/>""",
    """<EventID>({event_code}5157)<""",
    """<Computer>({host}[\w\-.]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data Name(\\)?=['"]+ProcessID['"]+>({process_id}[^<>]+)<\/Data>""",
    """<Data Name(\\)?=['"]+Application['"]+>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))<\/Data>""",
    """<Data Name(\\)?=['"]+SourceAddress['"]+>({src_ip}[a-fA-F:\d.]+)</Data>""",
    """<Data Name(\\)?=['"]+SourcePort['"]+>({src_port}\d+)</Data>""",
    """<Data Name(\\)?=['"]+DestAddress['"]+>({dest_ip}[a-fA-F:\d.]+)</Data>""",
    """<Data Name(\\)?=['"]+DestPort['"]+>({dest_port}\d+)</Data>""",
    """<Data Name(\\)?=['"]+Protocol['"]+>({protocol}[^<>]+)</Data>""",
    """<RenderingInfo.+?<Task>({operation_type}[^<>]+)</Task>.*?</RenderingInfo>""",
    """<Computer>({src_host}[\w\-.]+)<\/Computer>[\s\S]+?Direction['"]+>({direction}Outbound)""",
    """<Computer>({dest_host}[\w\-.]+)<\/Computer>[\s\S]+?Direction['"]+>({direction}Inbound)""",
    """<Computer>({src_host}[\w\-.]+)</Computer>[\s\S]+?Direction:\s*({direction}Outbound)""",
    """<Computer>({dest_host}[\w\-.]+)</Computer>[\s\S]+?Direction:((?-i)\\+[rnt])*\s*({direction}Inbound)""",
    """<Data Name(\\)?=['"]+LayerName['"]+>({layer_name}[^<]+)"""
    """Layer Name:\s+({layer_name}[^:]+?)\s+Layer Run-Time ID:"""
    """<Message>({failure_reason}.+?)\s*(:|\.)"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```