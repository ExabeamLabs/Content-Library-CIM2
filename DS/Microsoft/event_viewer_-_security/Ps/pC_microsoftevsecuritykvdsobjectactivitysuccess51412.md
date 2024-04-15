#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-activity-success-5141-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
time_createdFormat = ["yyyy-MM-dd HH:mm:ss"]
Conditions = [
  """EventID=5141"""
  """A directory service object was deleted"""
]
Fields = [
  """({event_name}A directory service object was deleted)"""
  """DetectTime=({time_created}\d{1,4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})\s+\w+="""
  """ComputerName =({host}[\w.\-]+)"""
  """EventID=({event_code}\w+)"""
  """Account Name =({user}.+?)\s+"""
  """Account Domain=({domain}.+?)\s"""
  """Logon ID=({login_id}[^\s]+)\s"""
  """Object:Class=({object_class}.+?)\s"""
  """Object:DN=({object_dn}.+?)\s*Object:GUID="""
  """Object:DN=.+?({object_ou}OU.+?)\s*Object:GUID"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```