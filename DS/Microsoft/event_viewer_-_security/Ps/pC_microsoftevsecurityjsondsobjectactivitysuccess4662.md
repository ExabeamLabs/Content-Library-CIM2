#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-activity-success-4662"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""An operation was performed on an object"""
""""EventID":4662"""
""""SourceName":"Microsoft-Windows-Security-Auditing""""
]
Fields = [
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""Computer":"({host}[^"]+)""""
""""Hostname":"({host}[^"]+)"""
"""({event_name}An operation was performed on an object)"""
"""({event_code}4662)"""
""""EventTime":\s*"?({time}[^",]+)"""
""""EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""""
""""SubjectUserSid":"({user_sid}[^"]+)""""
""""SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
""""SubjectDomainName":"({src_domain}({domain}[^"]+))""""
""""ObjectName":"({object}({object_name}[^"]+))""""
""""ObjectServer":"({object_server}[^"]+)""""
""""ObjectType":"({object_type}[^"]+)""""
""""LogonID":"({login_id}[^"]+)""""
""""OperationType":"({operation}[^"]+)""""
""""Properties":"(-|({properties}[^"]+))""""
""""AdditionalInfo":"(?:-|({additional_info}[^"]+))""""
""""AccessList":"(\\[srnt])*(-|({access}[^:]+?))(\\[srnt])*""""
"""Accesses:(\\[srnt])*(-|({access}[^:]+?))(\\[srnt])*Access Mask:"""
]
ParserVersion = "v1.0.0"


}
```