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
""""OperationType":""""
]
Fields = [
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""""
""""Computer":"({host}[^"]+)""""
""""Hostname":"({host}[^"]+)"""
"""({event_name}An operation was performed on an object)"""
"""({event_code}4662)"""
""""EventTime":\s*"?({time}[^",]+)"""
""""EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""""
""""SubjectUserSid":"({user_sid}[^"]+)""""
""""SubjectUserName":"({user}[^"]+)""""
""""SubjectDomainName":"({domain}[^"]+)""""
""""ObjectName":"({object}[^"]+)""""
""""ObjectServer":"({ds_object_class}[^"]+)""""
""""ObjectType":"({object_type}[^"]+)""""
""""LogonID":"({login_id}[^"]+)""""
""""OperationType":"({operation}[^"]+)""""
""""Properties":"(-|({properties}[^"]+))""""
""""AdditionalInfo":"(?:-|({additional_info}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```