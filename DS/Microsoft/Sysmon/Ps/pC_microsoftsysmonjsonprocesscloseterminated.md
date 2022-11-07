#### Parser Content
```Java
{
Name = microsoft-sysmon-json-process-close-terminated
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Microsoft-Windows-Sysmon""", """Process terminated:""", """"AccountName":"""" ]
  Fields = [
    """"UtcTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"Image":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """"TargetFilename":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
    """"Domain":"(NT AUTHORITY|({domain}[^"]+))""",
    """"AccountName":"((?i)SYSTEM|({user}[^"]+))""",
    """"SourceProcessId":"({process_id}\d+)""",
    """"SourceProcessGuid":"({process_guid}[^"]+)""",
    """"TargetProcessId":"({dest_process_id}\d+)""",
# target_process_guid is removed
    """"LogonId":"({login_id}[^"]+)""",
    """"Hostname":"({host}[^"]+)""",
    """"TargetImage":"({dest_process}({dest_process_dir}[^"]*?[\\\/]+)?({dest_process_name}[^"\\\/]+))"""",
    """"EventID":({event_code}\d+)""",
    """"ProcessGuid":"({process_guid}[^"]+)""",
    """"ProcessID":({process_id}\d+)""",
    """({log_name}Microsoft-Windows-Sysmon)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```