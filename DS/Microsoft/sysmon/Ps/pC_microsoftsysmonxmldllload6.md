#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-dll-load-6
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>6</EventID>""", """<EventRecordID>""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """({event_name}Driver loaded)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Security UserID='({user_sid}.+?)'\/>""",
    """<Data Name ='ImageLoaded'>({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<]+))))<\/Data>""",
    """<Data Name ='Hashes'>[^<>]*?MD5=({hash_md5}[^,<]+)""",
    """({log_name}Microsoft-Windows-Sysmon)"""
  ]
  DupFields = [ "host->dest_host", "event_name->operation" ]


}
```