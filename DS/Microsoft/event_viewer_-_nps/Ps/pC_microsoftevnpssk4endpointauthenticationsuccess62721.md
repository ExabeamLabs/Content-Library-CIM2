#### Parser Content
```Java
{
Name = microsoft-evnps-sk4-endpoint-authentication-success-6272-1
  Product = Event Viewer - NPS
  ParserVersion = v1.0.0
  Conditions = [ """"Activity":"6272 - Network Policy Server granted access to a user."""", """"EventID":6272""", """"EventSourceName":"Microsoft-Windows-Security-Auditing"""", """"Type":"SecurityEvent"""" ]
  Fields = ${WindowsParsersTemplates.json-windows-events-3.Fields}[
    """({event_name}Network Policy Server granted access to a user)""",
    """"AuthenticationType":"({auth_type}[^"]+)"""",
    """"EAPType":"(-|({auth_type}[^"]+))"""",
    """"NASIPv(4|6)Address":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"AuthenticationServer":"({auth_server}[^"]+)"""",
    """"CallingStationID":"(-|({src_mac}[^"]+))"""",
    """"FullyQualifiedSubjectMachineName":"(-|({user_type}[^"]+))"""",
    """"SubjectUserName":"((?:host\/)({src_host}[^"]+)|({email_address}[^@"]+@[^"]+)|(({email_domain}[^\\"]+)\\+)?({user}[^"]+))""""
  ]

json-windows-events-3 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"EventID":"?({event_code}\d+)"?""",
    """"Computer":"({host}[^"]+)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"SubjectUserName":"(-|({user}[^"\/]+))"""",
    """"SubjectDomainName":"(-|({domain}[^"]+))""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"EventSourceName":"({log_source}[^"]+)"""",
    """"IpPort":"({src_port}\d{1,5})"""
    """Source Port(=|:)\s*({src_port}\d+)"""
  
}
```