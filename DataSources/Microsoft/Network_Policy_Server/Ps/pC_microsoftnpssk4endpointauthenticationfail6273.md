#### Parser Content
```Java
{
Name = microsoft-nps-sk4-endpoint-authentication-fail-6273
  Product = Network Policy Server
  ParserVersion = v1.0.0
  Conditions = [ """"Activity":"6273 - Network Policy Server denied access to a user."""", """"EventID":"6273"""", """"EventSourceName":"Microsoft-Windows-Security-Auditing"""", """"Type":"SecurityEvent"""" ]
  Fields = ${WindowsParsersTemplates.json-windows-events-3.Fields}[
    """({event_name}Network Policy Server denied access to a user)""",
    """"NASIPv(4|6)Address":"({dest_ip}[a-fA-F\d:.]+)"""",
    """<Data Name\\?="Reason">({failure_reason}[^<]+)""",
    """"AuthenticationProvider":({auth_server}[^"]+)"""",
    """"FullyQualifiedSubjectMachineName":"(-|({user_type}[^"]+))"""",
    """"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({email_address}[^@"]+@[^"]+)|(({domain}[^\\"]+)\\+)?({user}[^"]+))"""",
    """NASIdentifier":"(({location}[\w.-]+))""""
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