#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-remove-success-memberremoved"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""event_id":"""
"""Microsoft-Windows-Security-Auditing"""
"""A member was removed from a security-enabled"""
]
Fields = [
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
""""+created"+:"+({time}[^"]+)"""
"""requestClientApplication=({app}[^=]+?)\s\w+="""
"""({event_name}An account was logged off)"""
""""keywords"+:\["+({result}[^"]+)"""
""""pid"+:({process_id}\d+)"""
"""thread"+:[^@]+?"+id"+:({thread_id}\d+)"""
""""TargetUserName"+:"+(None|({dest_user}[^"]+))"""
""""TargetDomainName"+:"+({domain}[^"]+)"""
""""TargetLogonId"+:"+({login_id}[^"]+)"""
""""LogonType"+:"+({login_type}\d+)"""
""""TargetUserSid"+:"+({user_sid}[^"<,]+)"""
""""record_id"+:({event_id}\d+)"""
""""task"+:"+({task_name}[^"]+)"""
""""event_id"+:({event_code}\d+)"""
""""(?:winlog\.)?computer_name"+:"+({src_host}[^"]+)"""
""""hostname"+:"+({host}[^"]+)"""
""""action"+:"+({action}[^"]+)"""
""""os":[^@]+?"name":"({os}[^"]+)"""
""""SubjectLogonId"+:"+({login_id}[^"]+)"""
""""+activity_id"+:"+\{({activity_id}[^}]+)"""
""""+ProviderName"+:"+({provider_name}[^"]+)"""
""""+SubjectUserSid"+:"+({user_sid}[^"<,]+)"""
""""+SubjectDomainName"+:"+({domain}[^"]+)"""
""""user"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""""+SubjectUserName"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""""+PrivilegeList"+:"+(-|({privileges}[^"]+))"""
""""+SidHistory"+:"+(-|({sid_history}[^"]+))"""
""""Keywords":"({result}[^"]+)"""
"""({event_name}A member was removed from a security-enabled)"""
""""+MemberSid"+:"+(({dest_user_sid}S-\d+-[^"]+)|({account_id}[^"]+))"""
""""TargetSid":"({group_id}[^\s"]+)"""
"""event_id"+:({event_code}\d+)"""
]
ParserVersion = "v1.0.0"


}
```