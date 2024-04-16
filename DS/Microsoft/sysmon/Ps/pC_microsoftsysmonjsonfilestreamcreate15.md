#### Parser Content
```Java
{
Name = microsoft-sysmon-json-file-stream-create-15
  Vendor = Microsoft
  ParserVersion = v1.0.0
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":15""", """"File stream created""", """FileCreateStreamHash""", """"SourceModuleType""" ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"Hostname":"({host}[^"]+)"""",
    """"AccountName":"((?i)SYSTEM|({user}[\w\.\-]{1,40}\$?))"""",
    """"EventID":({event_code}\d+)""",
    """"Domain":"((?i)NT AUTHORITY|NT-AUTORIT|({domain}[^"\\]+))"""",
    """"UserID":"({user_sid}[^"]+)"""",
    """"Category":"({event_name}[^(]+?)\s\(""",
    """"Severity":"({severity}[^"]+)"""",
    """"Image":"({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+)))"""",
    """"TargetFilename":"({file_path}({file_dir}[^"]*?)(\\+({file_name}[^"\\]+)))""""
    """({log_name}Microsoft-Windows-Sysmon)"""
  ]
  DupFields = [ "host->dest_host", "file_path->target" ]


}
```