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
""""SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
""""SubjectDomainName":"({domain}[^"]+)""""
""""ObjectName":"({ds_object_name}[^"]+)""""
""""ObjectServer":"({ds_object_class}[^"]+)""""
""""ObjectType":"({ds_object_type}[^"]+)""""
""""LogonID":"({login_id}[^"]+)""""
""""OperationType":"({operation}[^"]+)""""
""""Properties":"(-|({properties}[^"]+))""""
""""AdditionalInfo":"(?:-|({additional_info}[^"]+))""""
""""AccessList":"(\\[srnt])*(-|({access}[^:]+?))(\\[srnt])*""""
"""Accesses:(\\[srnt])*(-|({access}[^:]+?))(\\[srnt])*Access Mask:"""
]
DupFields = [ "ds_object_name->object" ]
ParserVersion = "v1.0.0"


}
```