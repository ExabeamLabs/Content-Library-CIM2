#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-521
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Unable to log events to security log:""", """521""" ]
  Fields = [
    """"EventID"*:"*({event_code}[^,"]+)""",
    """"TimeCreated":"[\\\/]*Date\(({time}\d{13})"""
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Hostname"*:"*({host}[^"]+)"""",
    """"EventType"*:"*({result}[^"]+)""",
    """"Domain"*:"*(-|({domain}[^"]+))""",
    """"Severity"*:"*({severity}[^"]+)"""",
    """"SeverityValue"*:({severity}[^,]+)""",
    """"AccountName"*:"*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"SubjectUserSid"*:"*({user_sid}[^"]+)"""",
    """"SubjectUserName"*:"*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"SubjectDomainName"*:"*(-|({domain}[^"]+))"""",
    """"LogonID"*:"*({login_id}[^"]+)"""",
    """"ProcessId"*:"*(\\t)*({process_id}[^\\"]+)"""",
    """"ProcessName"*:"*({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"param1"*:"*({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"TransactionId"*:"*({transaction_id}[^"]+)"""",
    """"Category"*:"*({event_name}[^"]+)""",
    """"Message"*:"*({event_name}[^.]+)""",
    """({event_name}Unable to log events to security log)""",
    """Status code:\s*[\\t]*({result_code}\w+)[\rn]*""",
    """"Level"*:({run_level}\d+)"""
# CrashOnAuditFail is removed
# number_of_failed_audits is removed

      """exa_json_path=$.Id,exa_field_name=event_code"""
      """exa_json_path=$.TimeCreated,exa_regex=[\\\/]*Date\(({time}\d{13})"""
      """exa_json_path=$.EventTime,exa_field_name=time"""
      """exa_json_path=$.ProcessId,exa_field_name=process_id"""
      """exa_json_path=$.Message,exa_field_name=event_name"""
      """exa_regex=({event_name}Unable to log events to security log)"""
      """exa_regex=Status code:\s*[\\t]*({result_code}\w+)[\rn]*"""
      """exa_json_path=$.Level,exa_field_name=run_level"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```