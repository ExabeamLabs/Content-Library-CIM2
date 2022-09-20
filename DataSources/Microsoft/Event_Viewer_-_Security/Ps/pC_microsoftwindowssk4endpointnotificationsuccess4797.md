#### Parser Content
```Java
{
Name = microsoft-windows-sk4-endpoint-notification-success-4797
   ParserVersion = v1.0.0
   Conditions = [ """"Activity":"4797 - An attempt was made to query the existence of a blank password for an account."""", """"EventID":"4797"""", """"EventSourceName":"Microsoft-Windows-Security-Auditing"""", """"Type":"SecurityEvent"""" ]
   Fields = ${DLWindowsParsersTemplates.json-windows-system-info.Fields}[
     """({event_name}An attempt was made to query the existence of a blank password for an account)""",
     """"TargetUserName":"({dest_user}[^"]+)"""",
     """"TargetDomainName":"({dest_domain}[^"]+)"""",
     """"TargetSid":"({dest_user_sid}[^"]+)"""",
     """"Workstation":"({src_host_windows}[^"]+)""""
   ]
 
json-windows-system-info = {
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