#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-endpoint-lock-success-4800
  ParserVersion = v1.0.0
  Conditions = [ """"Activity":"4800 - A session was disconnected from a Window Station."""", """"EventID":"4800"""", """"EventSourceName":"Microsoft-Windows-Security-Auditing"""", """"Type":"SecurityEvent"""" ]
  Fields = ${WindowsParsersTemplates.json-windows-events-3.Fields}[
    """({event_name}A session was disconnected from a Window Station)""",
    """"TargetUserName":"({dest_user}[^"]+)"""",
    """"TargetDomainName":"({dest_domain}[^"]+)"""",
    """"TargetSid":"({dest_user_sid}[^"]+)"""",
  ]

json-windows-events-3 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"EventID":"({event_code}\d+)"""",
    """"Computer":"({host}[^"]+)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"SubjectUserName":"(-|({user}[^"\/]+))"""",
    """"SubjectDomainName":"(-|({domain}[^"]+))""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"IpAddress":"({src_ip}[a-fA-F\d:.]+)"""",
    """"EventSourceName":"({log_source}[^"]+)"""",
    """"IpPort":"({src_port}\d{1,5})"""
  
}
```