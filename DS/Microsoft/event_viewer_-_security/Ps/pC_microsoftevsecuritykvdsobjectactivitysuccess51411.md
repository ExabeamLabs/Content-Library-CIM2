#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-activity-success-5141-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """EventCode=5141"""
  """A directory service object was deleted"""
]
Fields = [
  """({event_name}A directory service object was deleted)"""
  """({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
  """ComputerName =({host}[\w.\-]+)"""
  """EventCode=({event_code}\w+)"""
  """Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)"""
  """Object:.+?Class:\s+({object_type}.+?)\s+Operation:"""
  """Object:\s+DN:\s+({ds_object_dn}.+?)\s+GUID:"""
  """Object:\s+DN:.+?({ds_object_ou}OU.+?)\s+GUID:"""
]
ParserVersion = "v1.0.0"


}
```