#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-activity-success-4667
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """EventID="4667"""", """An application client context was deleted.""", """Microsoft-Windows-Security-Auditing""", """RecordNumber=""", """EventType=""", """Channel=""" ]
  Fields = ${DLWindowsParsersTemplates.windows-system-info.Fields}[
    """(Client)?Domain="({domain}[^"]+)"""",
    """ClientName ="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+)\-\d+:\d+\s({host}[^\s]+)""",
    """Application Information:\s+({additional_info}[^@]+?)\s*$""",
    """({event_name}An application client context was deleted)"""
  ]

windows-system-info = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Fields = [
    """"EventID":"({event_code}\d+)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"EventSourceName":"({log_source}[^"]+)"""",
    """"IpPort":"({src_port}\d{1,5})"""
  
}
```