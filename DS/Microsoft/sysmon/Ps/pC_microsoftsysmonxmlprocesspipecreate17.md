#### Parser Content
```Java
{
Name = microsoft-sysmon-xml-process-pipe-create-17
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """<EventID>17<""", """'Microsoft-Windows-Sysmon'""", """<Data Name ='PipeName'"""]
  Fields = [
    """<Data Name\\*='UtcTime'>({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d+)<\/Data>""",
    """<Computer>({host}[^<]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Data Name\\*='ProcessId'>({process_id}\d+)<\/Data>""",
# pipe_name is removed
    """<Data Name\\*='Image'>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?)?)<\/Data>""",
    """<Data Name\\*='ProcessGuid'>({process_guid}[^<]+)<\/Data>""",
    """<Data Name\\*='EventType'>({event_name}[^<]+)<\/Data>""",
    """<Security UserID\\*='({user_sid}[^']+)'"""
    """({log_name}Microsoft-Windows-Sysmon)""" 
  ]


}
```