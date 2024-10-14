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
"""<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({src_host}({host}[^<]+))"""
 """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}[^<]+)"""
"""<Data Name(\\)?=('|")SubjectUserName('|")>(-|CN=[^<]+|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<"""
"""<Data Name(\\)?=('|")SubjectDomainName('|")>(-|({domain}[^<]+))"""
"""<Data Name(\\)?=('|")SubjectLogonId('|")>({login_id}[^<]+)"""
"""<Data Name(\\)?=('|")ObjectServer('|")>({ds_object_class}[^<]+)"""
"""<Data Name(\\)?=('|")ObjectType('|")>({ds_object_type}[^<]+)"""
"""<Data Name(\\)?=('|")ObjectName('|")>({ds_object_name}[^<]+)"""
"""<Data Name(\\)?=('|")OperationType('|")>({operation}[^<]+)"""
"""<Data Name(\\)?=('|")Properties('|")>\s*(-|({properties}[^<]+?))\s*<"""
"""<Keyword>({result}[^<]+)<"""
"""<Data Name\\*='AccessList'>(-|({access}[^<]+?))\s*<"""
"""Accesses:\s*(-|({access}[^:]+?))\s+Access Mask:"""
"""<Data Name\\*='AccessMask'>(-|({access_mask}[^<]+?))\s*<"""
"""<Data Name\\*='AccessList'>(-|({access_list}[^<]+?))\s*<"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```