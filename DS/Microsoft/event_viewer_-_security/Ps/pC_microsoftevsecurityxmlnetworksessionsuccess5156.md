#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-session-success-5156
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
"""<EventID>5156</EventID>""",
"""<Event xmlns"""
  ]
  Fields = [
    """({event_name}The Windows Filtering Platform has permitted a connection)""",
    """<TimeCreated SystemTime\\*='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({event_code}5156)""",
    """<Computer>({host}[^<>]+)</Computer>""",
    """<Data Name\\*='ProcessID'>({process_id}[^<>]+)<\/Data>""",
    """<Data Name\\*='Application'>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))<\/Data>""",
    """<Data Name\\*='SourceAddress'>(::1|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?<\/Data>""",
    """<Data Name\\*='SourcePort'>({src_port}\d+)</Data>""",
    """<Data Name\\*='DestAddress'>(::1|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({dest_port}\d+))?<\/Data>""",
    """<Data Name\\*='DestPort'>({dest_port}\d+)<\/Data>""",
    """<Data Name\\*='Protocol'>({protocol}[^<>]+)<\/Data>""",
    """<RenderingInfo[^$]+?<Task>({operation_type}}[^<>]+)</Task>[^$]*?</RenderingInfo>""",
    """<Computer>({src_host}[^<>]+)</Computer>[^$]+?Direction:\s*({direction}Outbound)""",
    """<Computer>({dest_host}[^<>]+)</Computer>[^$]+?Direction:\s*({direction}Inbound)""",
    """Layer Name:\s*({layer_name}[^:]+?)(\\[rn]|\s)"""
  ]
  DupFields = [ "host->local_asset" ]


}
```