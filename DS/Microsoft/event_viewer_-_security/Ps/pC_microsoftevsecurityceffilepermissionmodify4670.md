#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-file-permission-modify-4670
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Permissions on an object were changed""", """"EventID":4670""", """Microsoft-Windows-Security-Auditing""", """ cs6=""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({host}[\w\-.]+)"""",
    """({event_name}Permissions on an object were changed)""",
    """({event_code}4670)""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """"SubjectDomainName":"({src_domain}({domain}[^"]+))"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"ProcessId":"({process_id}[^"]+)"""",
    """"ProcessName":"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]+))"""",
    """"HandleId":"({object_id}[^"]+)"""",
    """"ObjectType":"({object_type}[^"]+)"""",
    """"ObjectName":"(-|({object_name}[^"]+))"""",
    """"OldSd\\?">?({old_attribute}[^"<]+)""",
    """"NewSd\\?">?({new_attribute}[^"<]+)""",
    """"Level":"({run_level}[^"]+)"""",
    """"_ResourceId":"({resource}[^"]+)""""
  ]
  ParserVersion = v1.0.0


}
```