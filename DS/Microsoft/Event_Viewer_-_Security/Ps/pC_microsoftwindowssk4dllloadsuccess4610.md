#### Parser Content
```Java
{
Name = microsoft-windows-sk4-dll-load-success-4610
   ParserVersion = v1.0.0
   Conditions = [ """"Activity":"4610 - An authentication package has been loaded by the Local Security Authority."""", """"EventID":"4610"""", """"EventSourceName":"Microsoft-Windows-Security-Auditing"""", """"Type":"SecurityEvent"""" ]
   Fields = ${DLWindowsParsersTemplates.json-windows-system-info.Fields}[
     """({event_name}An authentication package has been loaded by the Local Security Authority)""",
     """"AuthenticationPackageName":"({auth_package}[^"]+)""""
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