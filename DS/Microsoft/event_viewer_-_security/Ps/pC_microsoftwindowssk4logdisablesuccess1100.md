#### Parser Content
```Java
{
Name = microsoft-windows-sk4-log-disable-success-1100
   ParserVersion = v1.0.0
   Conditions = [ """"Activity":"1100 - The event logging service has shut down."""", """"EventID":"1100"""", """"EventSourceName":"Microsoft-Windows-Eventlog"""", """"Type":"SecurityEvent"""" ]
   Fields = ${DLWindowsParsersTemplates.json-windows-system-info.Fields}[
     """({event_name}The event logging service has shut down)"""
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
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"EventSourceName":"({log_source}[^"]+)"""",
    """"IpPort":"({src_port}\d{1,5})"""
  
}
```