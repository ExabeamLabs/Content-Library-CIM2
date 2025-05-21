#### Parser Content
```Java
{
Name = microsoft-windows-sk4-endpoint-notification-success-4797
   ParserVersion = v1.0.0
   Conditions = [ """"Activity":"4797 - An attempt was made to query the existence of a blank password for an account."""", """"EventID":"4797"""", """"EventSourceName":"Microsoft-Windows-Security-Auditing"""", """"Type":"SecurityEvent"""" ]
   Fields = ${DLWindowsParsersTemplates.json-windows-system-info.Fields}[
     """"Computer":"({host}[^"]+)"""",
     """({event_name}An attempt was made to query the existence of a blank password for an account)""",
     """"TargetUserName":"({dest_user}[^"]+)"""",
     """"TargetDomainName":"({dest_domain}[^"]+)"""",
     """"TargetSid":"({dest_user_sid}[^"]+)"""",
     """"Workstation":"({src_host_windows}[^"]+)""""
   ]
   DupFields = ${DLWindowsParsersTemplates.json-windows-system-info.DupFields}[ "src_host_windows->src_host" ]
 
json-windows-system-info = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Fields = [
    """"EventID":"({event_code}\d+)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""",
    """"SubjectLogonId":"({login_id}[^"]+)""",
    """"SubjectUserName":"(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"SubjectDomainName":"(-|({domain}[^"]+))""",
    """"SubjectUserSid":"({user_sid}[^"]+)""",
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"EventSourceName":"({log_source}[^"]+)"""",
    """"IpPort":"({src_port}\d{1,5})"""
  ]
  DupFields = [ "user->src_user" , "domain->src_domain" 
}
```