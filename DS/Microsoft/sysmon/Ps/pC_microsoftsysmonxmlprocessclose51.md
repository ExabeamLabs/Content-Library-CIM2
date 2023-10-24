#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-process-close-5-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>5</EventID>""", """<Message>Process terminated:""" ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'\/>""",
    """<Computer>({dest_host}({host}[\w\-.]+))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """({event_name}Process terminated)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Security UserID\\*='({user_sid}.+?)'\/>""",
    """<Data Name\\*='ProcessGuid'>\{({process_guid}[^\}]+)""",
    """<Data Name\\*='ProcessId'>({process_id}.+?)<\/Data>""",
    """<Data Name\\*='Image'>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/<]+?))<\/Data>""",
    """({log_name}Microsoft-Windows-Sysmon)""",
  ]
  DupFields = [ "process_guid->process_id" ]


}
```