#### Parser Content
```Java
{
Name = microsoft-windows-sk4-group-list-success-4798
   ParserVersion = v1.0.0
   Conditions = [ """"Activity":"4798 - A user's local group membership was enumerated."""", """"EventID":"4798"""", """"EventSourceName":"Microsoft-Windows-Security-Auditing"""", """"Type":"SecurityEvent"""" ]
   Fields = ${DLWindowsParsersTemplates.json-windows-system-info.Fields}[
     """({event_name}A user's local group membership was enumerate)""",
     """"TargetUserName":"({dest_user}[^"]+)"""",
     """"TargetDomainName":"({dest_domain}[^"]+)"""",
     """"TargetSid":"({dest_user_sid}[^"]+)"""",
     """"CallerProcessId":"({process_id}[^"]+)"""",
     """"CallerProcessName":"(	process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\]+))""""
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