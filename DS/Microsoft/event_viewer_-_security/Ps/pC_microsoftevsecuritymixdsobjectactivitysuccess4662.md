#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-ds-object-activity-success-4662"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss" ,"epoch","yyyy-MM-dd'T'HH:mm:ss.SSS"]
Conditions = [
"""An operation was performed on an object"""
]
Fields = [
"""({event_name}An operation was performed on an object)"""
"""({event_code}4662)"""
"""({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+"""
""""time":({time}\d{13})"""
""""time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+)"""
"""Security ID:\s*((?-i)\\+[rnt])*(|({user_sid}.+?))\s*((?-i)\\+[rnt])*Account Name:"""
"""Account Name:\s*((?-i)\\+[rnt])*(({full_name}[^:]+?\s[^\s]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*((?-i)\\+[rnt])*Account Domain:"""
"""Account Domain:\s*((?-i)\\+[rnt])*(|({domain}.+?))\s*((?-i)\\+[rnt])*Logon ID:"""
"""Object Server:\s*((?-i)\\+[rnt])*(|({object_server}.+?))\s*((?-i)\\+[rnt])*Object Type:"""
"""Object Type:\s*((?-i)\\+[rnt])*(|({object_type}.+?))\s*((?-i)\\+[rnt])*Object Name:"""
"""Object Name:\s*((?-i)\\+[rnt])*(|({object_name}.+?))\s*((?-i)\\+[rnt])*Handle ID:"""
"""Logon ID:\s*((?-i)\\+[rnt])*({login_id}[^:]+?)[\\n\s]*Object:"""
"""Operation Type:\s*({operation}.+?)\s+Accesses:"""
"""Properties:\s*({properties}.+?)\s+Additional"""
"""Additional Information:\s*(|({attribute}.*?))(\\n)*\s*"""
"""Accesses:\s*((?-i)\\+[rnt])*({access}[^:]+?)\s*((?-i)\\+[rnt])*Access Mask:"""
]
DupFields = [ "object_name->object" ]
ParserVersion = "v1.0.0"


}
```