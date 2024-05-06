#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-create-success-4720-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
""""event_id":4720"""
"""Microsoft-Windows-Security-Auditing"""
"""A user account was created"""
]
Fields = [
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
""""+created"+:"+({time}[^"]+)"""
"""requestClientApplication=({app}[^=]+?)\s\w+="""
"""({event_name}An account was logged off)"""
""""keywords"+:\["+({result}[^"]+)"""
""""pid"+:({process_id}\d+)"""
"""thread"+:[^@]+?"+id"+:({thread_id}\d+)"""
""""TargetUserName"+:"+(None|({dest_user}[\w\.\-]{1,40}\$?)|({dest_user_full_name}[^"]+))""""
""""TargetDomainName"+:"+({domain}[^"]+)"""
""""TargetLogonId"+:"+({login_id}[^"]+)"""
""""LogonType"+:"+({login_type}\d+)"""
""""TargetUserSid"+:"+({user_sid}[^"<,]+)"""
""""record_id"+:({event_id}\d+)"""
""""task"+:"+({task_name}[^"]+)"""
""""event_id"+:({event_code}\d+)"""
""""(?:winlog\.)?computer_name"+:"+({src_host}[^"]+)"""
""""hostname"+:"+({host}[\w\-.]+)"""
""""action"+:"+({action}[^"]+)"""
""""os":[^@]+?"name":"({os}[^"]+)"""
""""SubjectLogonId"+:"+({login_id}[^"]+)"""
""""+activity_id"+:"+\{({activity_id}[^}]+)"""
""""+ProviderName"+:"+({provider_name}[^"]+)"""
""""+SubjectUserSid"+:"+({user_sid}[^"<,]+)"""
""""+SubjectDomainName"+:"+({domain}[^"]+)"""
""""user"+:"+(SYSTEM|-|({user}[\w\.\-]{1,40}\$?))"""
""""+SubjectUserName"+:"+(SYSTEM|-|({user}[\w\.\-]{1,40}\$?))"""
""""Keywords":"({result}[^"]+)"""
"""({event_name}A user account was created)"""
"""exa_json_path=$..created,exa_field_name=time""",
"""exa_json_path=$.message,exa_regex=({event_name}A user account was created)""",
"""exa_regex="keywords"+:\["+({result}[^"]+)""",
"""exa_json_path=$..pid,exa_field_name=process_id""",
"""exa_json_path=$..thread.id,exa_field_name=thread_id""",
"""exa_json_path=$..TargetUserName,exa_regex=^(None|({dest_user}[\w\.\-]{1,40}\$?)|({dest_user_full_name}[^"]+))$""",
"""exa_json_path=$..TargetDomainName,exa_field_name=domain""",
"""exa_json_path=$..TargetSid,exa_field_name=user_sid""",
"""exa_json_path=$..record_id,exa_field_name=event_id""",
"""exa_json_path=$..task,exa_field_name=task_name""",
"""exa_json_path=$..event_id,exa_field_name=event_code""",
"""exa_json_path=$..computer_name,exa_regex=^({src_host}[\w\-.]+)$""",
"""exa_json_path=$.host.hostname,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$..action,exa_field_name=action""",
"""exa_json_path=$..os.name,exa_field_name=os""",
"""exa_json_path=$..SubjectLogonId,exa_field_name=login_id""",
"""exa_json_path=$..provider_name,exa_field_name=provider_name""",
"""exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
"""exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
"""exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({user}[\w\.\-]{1,40}\$?))$"""
]
ParserVersion = "v1.0.0"


}
```