#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-file-time-modify-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>2</EventID>""", """<Message>File creation time changed:""" ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'\/>""",
    """<Computer>({dest_host}({host}[^<>]+))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """({event_name}File creation time changed)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Security UserID\\*='({user_sid}[^>]+?)'\/>""",
    """<Data Name\\*='ProcessGuid'>\{({process_guid}[^\}]+)""",
    """<Data Name\\*='ProcessId'>({process_id}[^<]+?)<\/Data>""",
    """<Data Name\\*='Image'>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/<]+?))<\/Data>""",
    """<Data Name\\*='TargetFilename'>({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<]+))))<\/Data>""",
    """<Provider Name\\*='({log_name}[^']+)'"""
  ]
  DupFields = [ "event_name->access" ]


}
```