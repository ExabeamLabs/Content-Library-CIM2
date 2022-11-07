#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-endpoint-activity-success-microsoftwindowssecurityauditing
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [  """Microsoft-Windows-Security-Auditing[""", """"EventID":""" ]

json-windows-system-events = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"EventID"*:"*({event_code}[^,"]+)""",
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"Hostname"*:"*({host}[^"]+)"""",
    """"EventType"*:"*({result}[^"]+)""",
    """"Domain"*:"*(-|({domain}[^"]+))""",
    """"Severity"*:"*({severity}[^"]+)"""",
    """"SeverityValue"*:({severity}[^,]+)""",
    """"AccountName"*:"*({user}[^"]+)"""",
    """"SubjectUserSid"*:"*({user_sid}[^"]+)"""",
    """"SubjectUserName"*:"*({user}[^"]+)"""",
    """"SubjectDomainName"*:"*(-|({domain}[^"]+))"""",
    """"LogonID"*:"*({login_id}[^"]+)"""",
    """"ProcessId"*:"*(\\t)*({process_id}[^\\"]+)"""",
    """"ProcessName"*:"*({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"param1"*:"*({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"TransactionId"*:"*({transaction_id}[^"]+)"""",
    """"Category"*:"*({event_name}[^"]+)""",
    """"Message"*:"*({event_name}[^.]+)""",
  
}
```