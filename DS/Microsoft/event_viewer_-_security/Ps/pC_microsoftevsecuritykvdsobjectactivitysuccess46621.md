#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-activity-success-4662-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """,4662,"""
  """An operation was performed on an object"""
]
Fields = [
  """({event_name}An operation was performed on an object)"""
  """(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+),"""
  """({action}(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)),({host}[\w\-.]+)"""
  """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain"""
  """Account Domain:\s*({domain}.+?)\s*Logon ID"""
  """Logon ID:\s*({login_id}[^\s]+)"""
  """Object Server:\s*({object_server}.+?)\s*Object Type:"""
  """Object Type:\s*({object_type}.+?)\s*Object Name:"""
  """Object Name:\s*({object_name}.+?)\s*Handle ID:"""
  """Operation Type:\s*({action}.+?)\s*Accesses:"""
  """Properties:\s*(?:-|({properties}.+?))\s*Additional Information:"""
  """Additional Information:\s*({attribute}[^,]+)"""
  """({event_code}4662)"""
  """Accesses:\s*({access}[^:]+?)\s*Access Mask:"""
]
DupFields = [
  "object_name->object"
]
ParserVersion = "v1.0.0"


}
```