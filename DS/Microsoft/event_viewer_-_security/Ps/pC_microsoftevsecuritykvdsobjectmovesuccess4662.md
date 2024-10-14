#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-move-success-4662"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""EventIDCode=4662"""
]
Fields = [
  """Computer=\s*({host}[\w\-.]*)"""
  """EventID=({event_code}\d+)"""
  """TimeGenerated=({time}\d{10})"""
  """Message=({event_name}.*?)\s+Subject:"""
  """Security ID:\s*({user_sid}\S+)\s+Account Name:"""
  """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:"""
  """Account Domain:\s*({domain}\S+)\s+Logon ID:"""
  """Logon ID:\s*({login_id}\S+)\s+Object:"""
  """Object Server:\s*({ds_object_class}\S.*?)\s+Object Type:"""
  """Object Type:\s*({ds_object_type}\S+)\s*Object Name:"""
  """Object Name:\s*({ds_object_name}\S.*?)\s*Handle ID:"""
  """Operation Type:\s*({operation_type}\S.*?)\s*Accesses:"""
  """Accesses:\s*({access}\S.*?)\s*Access Mask:"""
  """Properties:\s*({attributes}\S.*?)\s*Additional Information:"""
]
DupFields = [
"ds_object_name->object"
]
ParserVersion = "v1.0.0"


}
```