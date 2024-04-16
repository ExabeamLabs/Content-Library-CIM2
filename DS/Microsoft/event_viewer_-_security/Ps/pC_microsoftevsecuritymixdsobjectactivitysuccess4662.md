#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-ds-object-activity-success-4662"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""An operation was performed on an object"""
]
Fields = [
"""({event_name}An operation was performed on an object)"""
"""({event_code}4662)"""
"""({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+"""
"""Security ID:\s*(|({user_sid}.+?))\s*Account Name:"""
"""Account Name:\s*(({full_name}[^:]+?\s[^\s]+?)|({user}[\w\.\-]{1,40}\$?))\s*Account Domain:"""
"""Account Domain:\s*(|({domain}.+?))\s*Logon ID:"""
"""Object Server:\s*(|({ds_object_class}.+?))\s*Object Type:"""
"""Object Type:\s*(|({ds_object_type}.+?))\s*Object Name:"""
"""Object Name:\s*(|({ds_object_name}.+?))\s*Handle ID:"""
"""Logon ID:\s*({login_id}[^:]+?)[\\n\s]*Object:"""
"""Operation Type:\s*({operation}.+?)\s+Accesses:"""
"""Properties:\s*({properties}.+?)\s+Additional"""
"""Additional Information:\s*(|({attribute}.*?))(\\n)*\s*"""
"""Accesses:\s*({access}[^:]+?)\s*Access Mask:"""
]
DupFields = [ "ds_object_name->object" ]
ParserVersion = "v1.0.0"


}
```