#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-activity-success-4662"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4662<"""
]
Fields = [
"""({event_name}An operation was performed on an object)"""
"""<EventID>({event_code}\d+)"""
"""<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[^<]+)"""
"""<Data Name(\\)?='SubjectUserSid'>({user_sid}[^<]+)"""
"""<Data Name(\\)?='SubjectUserName'>(-|CN=[^<]+|({user}[^<]+))"""
"""<Data Name(\\)?='SubjectDomainName'>(-|({domain}[^<]+))"""
"""<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)"""
"""<Data Name(\\)?='ObjectServer'>({ds_object_class}[^<]+)"""
"""<Data Name(\\)?='ObjectType'>({object_type}[^<]+)"""
"""<Data Name(\\)?='ObjectName'>({object}[^<]+)"""
"""<Data Name(\\)?='OperationType'>({operation}[^<]+)"""
"""<Data Name(\\)?='Properties'>\s*(-|({properties}[^<]+?))\s*<"""
"""<Keyword>({result}[^<]+)<"""
"""Accesses:\s*({access}[^:]+?)\s+Access Mask:"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```