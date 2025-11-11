#### Parser Content
```Java
{
Name = "microsoft-evsecurity-sk4-share-access-5145-8"
Conditions = [
""""EventId":5145"""
"""A network share object was checked to see whether client can be granted desired access"""
"""Microsoft-Windows-Security-Auditing"""
""""MachineName":"""
""""TimeCreated":"""
]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """"TargetUserName"+:"+(None|({dest_user}[^"]+))""",
    """"TargetDomainName"+:"+({dest_domain}[^"]+)""",
    """"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))""",
    """"user"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """"(?:winlog\.)?computer_name"+:"+({src_host}[\w\-.]+)""",
    """"hostname"+:"+({host}[\w\-.]+)""",
    """exa_json_path=$.winlog.event_data.TargetDomainName,exa_field_name=dest_domain"""
    """exa_json_path=$.winlog.event_data.SubjectDomainName,exa_field_name=domain"""
      """exa_json_path=$.winlog.event_data.SubjectDomainName,exa_field_name=src_domain"""
    """exa_json_path=$.winlog.event_data.TargetUserName,exa_field_name=dest_user""",
    """exa_json_path=$.winlog.event_data.SubjectUserName,exa_field_name=user""",
    """exa_json_path=$.winlog.event_data.SubjectUserName,exa_field_name=src_user""",
    """exa_json_path=$.winlog.computer_name,exa_field_name=src_host""",
    """exa_json_path=$.host.hostname,exa_field_name=host""",
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({host}[^"]+))"""
  
}
```