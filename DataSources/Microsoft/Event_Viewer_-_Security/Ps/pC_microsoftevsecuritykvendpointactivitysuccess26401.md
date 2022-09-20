#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-activity-success-26401
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """EventID="26401"""", """MOMSDK_Service_Security""", """RecordNumber=""", """EventType=""", """Channel=""" ]
  Fields = ${DLWindowsParsersTemplates.windows-system-info.Fields}[
    """AccountName ="({user}[^"]+)"\sUserID="({user_sid}[^"]+)"\sAccountType="User""""
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