#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-notification-5033
  ParserVersion = v1.0.0
  Conditions = [ """"EventID":"5033"""", """Microsoft-Windows-Security-Auditing""", """The Windows Firewall Driver has started successfully""" ]
  Fields = ${WindowsParsersTemplates.json-windows-events-3.Fields}[
    """"Computer":"({host}[^"]+)"""",
    """({event_name}The Windows Firewall Driver has started successfully)""",
    """({event_code}5033)"""
  ]

json-windows-events-3 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Fields = [
    """"EventID":"?({event_code}\d+)"?""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"SubjectUserName":"(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"SubjectDomainName":"(-|({domain}[^"]+))""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"EventSourceName":"({log_source}[^"]+)"""",
    """"IpPort":"({src_port}\d{1,5})"""
    """Source Port(=|:)\s*({src_port}\d+)"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"
}
```