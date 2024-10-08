#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-process-pipe-create-success-18
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Conditions = [ """<EventID>18</EventID>""", """<Provider Name =""", """Microsoft-Windows-Sysmo""" ]
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """<Data Name\\*='UtcTime'>({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d+)<\/Data>""",
    """<Computer>({host}[\w\-.]+)<\/Computer>""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Data Name\\*='ProcessId'>({process_id}\d+)<\/Data>""",
# pipe_name is removed
    """<Data Name\\*='Image'>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?)?)<\/Data>""",
    """<Data Name\\*='ProcessGuid'>({process_guid}[^<]+)<\/Data>""",
    """<Data Name\\*='EventType'>({event_name}[^<]+)<\/Data>""",
    """<Security UserID\\*='({user_sid}[^']+)'"""
    """({log_name}Microsoft-Windows-Sysmon)""" 
    """<Data Name\\*='User'>(({domain}[^\>]+?\w+))?\\({user}[^\<>]+)<\/Data>"""
  ]


}
```