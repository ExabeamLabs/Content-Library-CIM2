#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-activity-success-4665
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """EventID="4665"""", """An attempt was made to create an application client context.""", """Microsoft-Windows-Security-Auditing""", """RecordNumber=""", """EventType=""", """Channel=""" ]
  Fields = ${DLWindowsParsersTemplates.windows-system-info.Fields}[
    """Application Information:\s+({additional_info}[^@]+?)\s+Status:""",
    """({event_name}An attempt was made to create an application client context)"""
  ]

windows-system-info = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"EventID":"({event_code}\d+)"""",
    """"Computer":"({host}[^"]+)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"SubjectUserName":"(-|({user}[^"]+))""",
    """"SubjectDomainName":"(-|({domain}[^"]+))""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"IpAddress":"({src_ip}[a-fA-F\d:.]+)"""",
    """"EventSourceName":"({log_source}[^"]+)"""",
    """"IpPort":"({src_port}\d{1,5})"""
  
}
```