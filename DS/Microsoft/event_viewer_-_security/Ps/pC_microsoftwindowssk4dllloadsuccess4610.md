#### Parser Content
```Java
{
Name = microsoft-windows-sk4-dll-load-success-4610
   ParserVersion = v1.0.0
   Conditions = [ """"Activity":"4610 - An authentication package has been loaded by the Local Security Authority."""", """"EventID":"4610"""", """"EventSourceName":"Microsoft-Windows-Security-Auditing"""", """"Type":"SecurityEvent"""" ]
   Fields = ${DLWindowsParsersTemplates.json-windows-system-info.Fields}[
     """"SubjectDomainName":"(-|({src_domain}({domain}[^"]+)))""",
     """"SubjectUserName":"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
     """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"Computer":"({host}[^"]+)"""",
     """({event_name}An authentication package has been loaded by the Local Security Authority)""",
     """"AuthenticationPackageName":"({file_path}({file_dir}[^<]+)\\({file_name}[^:]+?))\s*:\s*({auth_package}[^<]+)""""
   ]
 
json-windows-system-info = {
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