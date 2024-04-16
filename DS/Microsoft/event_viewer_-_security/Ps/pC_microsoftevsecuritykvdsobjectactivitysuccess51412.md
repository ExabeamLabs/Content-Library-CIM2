#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-activity-success-5141-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [
  """EventID=5141"""
  """A directory service object was deleted"""
]
Fields = [
  """({event_name}A directory service object was deleted)"""
  """DetectTime=({time}\d{1,4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})\s+\w+="""
  """ComputerName =({host}[\w.\-]+)"""
  """EventID=({event_code}\w+)"""
  """Account Name =({user}[\w\.\-]{1,40}\$?)\s+"""
  """Account Domain=({domain}.+?)\s"""
  """Logon ID=({login_id}[^\s]+)\s"""
  """Object:Class=({ds_object_class}.+?)\s"""
  """Object:DN=({ds_object_dn}.+?)\s*Object:GUID="""
  """Object:DN=.+?({ds_object_ou}OU.+?)\s*Object:GUID"""
]
ParserVersion = "v1.0.0"


}
```