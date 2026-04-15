#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-assign-success-4673-1"
Conditions = [ """"EventID":"4673"""", """A privileged service was called""" ]
ExtractionType = json
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """"(?:winlog\.)?computer_name"+:"+({src_host}[\w\-.]+)""",
    """"hostname"+:"+({host}[\w\-.]+)""",
    """"TargetUserName"+:"+(None|({dest_user}[^"]+))""",
    """"user"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"+SubjectUserName"+:"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """"TargetDomainName"+:"+({dest_domain}[^"]+)""",
    """"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))""",
    """"Channel"+:"+({channel}[^"]+)"""
    """exa_json_path=$.winlog.event_data.TargetDomainName,exa_field_name=dest_domain""",
    """exa_json_path=$.winlog.event_data.SubjectDomainName,exa_field_name=domain""",
    """exa_json_path=$.winlog.event_data.SubjectDomainName,exa_field_name=src_domain""",
    """exa_json_path=$.winlog.event_data.TargetUserName,exa_field_name=dest_user""",
    """exa_json_path=$.winlog.event_data.SubjectUserName,exa_field_name=user""",
    """exa_json_path=$.winlog.event_data.SubjectUserName,exa_field_name=src_user""",
    """exa_json_path=$.winlog.computer_name,exa_field_name=src_host""",
    """exa_json_path=$.host.hostname,exa_field_name=host""",
    """exa_regex=({event_name}(A user account was locked out|Account That Was Locked Out))"""
    """exa_json_path=$..channel,exa_field_name=channel"""
  
}
```