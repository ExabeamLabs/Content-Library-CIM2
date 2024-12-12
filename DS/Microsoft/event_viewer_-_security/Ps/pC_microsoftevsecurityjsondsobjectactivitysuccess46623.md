#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-activity-success-4662-3"
Conditions = [
""""event_id":4662"""
"""An operation was performed on an object"""
""""SubjectDomainName":""""
""""provider":"Microsoft-Windows-Security-Auditing""""
]
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
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
""""hostname"+:"+({host}[\w\-.]+)"""
""""action"+:"+({action}[^"]+)"""
""""os":[^@]+?"name":"({os}[^"]+)"""
""""SubjectLogonId"+:"+({login_id}[^"]+)"""
""""+activity_id"+:"+\{({activity_id}[^}]+)"""
""""+ProviderName"+:"+({provider_name}[^"]+)"""
""""+SubjectUserSid"+:"+({user_sid}[^"<,]+)"""
""""+SubjectDomainName"+:"+({domain}[^"]+)"""
""""user"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""""+SubjectUserName"+:"+(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))""""
""""+PrivilegeList"+:"+(-|({privileges}[^"]+))"""
""""+SidHistory"+:"+(-|({sid_history}[^"]+))"""
""""Keywords":"({result}[^"]+)"""
""""Computer":"({host}[\w\-.]+)""""
""""TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({event_name}An operation was performed on an object)"""
"""({event_code}4662)"""
""""ObjectName":"({object_name}[^"]+)""""
""""ObjectServer":"({object_server}[^"]+)""""
""""ObjectType":"({object_type}[^"]+)""""
""""LogonID":"({login_id}[^"]+)""""
""""OperationType":"({operation}[^"]+)""""
""""AdditionalInfo":"(?:-|({additional_info}[^"]+))""""
""""AccessList":"(\\[srnt])*(-|({access}[^:]+?))(\\[srnt])*""""
"""Accesses:(\\[srnt])*(-|({access}[^:]+?))(\\[srnt])*Access Mask:"""
]
DupFields = [
"object_name->object"
]


}
```