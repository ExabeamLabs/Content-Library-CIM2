#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-activity-auditing
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""""SourceName":"Microsoft-Windows-Security-Auditing"""", """"EventID":"""]
  Fields = [
    """"EventID":({event_code}[^,]+)""",
    """"EventTime":({time}\d+)""",
    """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"Hostname":"({host}[^"]+)"""",
    """"Severity":"({severity}[^"]+)"""",
    """"SeverityValue":({severity}[^,]+)""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"({user}[^"]+)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"LogonID":"({login_id}[^"]+)"""",
    """"ProcessID":({process_id}\d+)""",
    """"ProcessId":"(\\t)*({process_id}[^\\]+)"""",
    """"ProcessName":"({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"param1":"({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"TransactionId":"({transaction_id}[^"]+)"""",
    """"Message":"({event_name}[^.]+)""",
  ]


}
```