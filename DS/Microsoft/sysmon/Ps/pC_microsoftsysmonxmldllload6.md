#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-dll-load-6
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>6</EventID>""", """<EventRecordID>""", """<Channel>Microsoft-Windows-Sysmon/Operational</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Computer>({dest_host}({host}[\w\-.]+))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """({event_name}Driver loaded)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Security UserID\\*='({user_sid}.+?)'\/>""",
    """<Data Name\\*=('|")ImageLoaded('|")>({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<]+))))<\/Data>""",
    """<Data Name\\*=('|")Hashes('|")>[^<>]*?MD5=({hash_md5}[^,<]+)""",
    """({log_name}Microsoft-Windows-Sysmon)"""
    """ThreadID(\\)?='({thread_id}\d+)"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "event_name->operation" ]


}
```