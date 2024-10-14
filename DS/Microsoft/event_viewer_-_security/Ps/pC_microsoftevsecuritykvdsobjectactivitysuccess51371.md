#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-activity-success-5137-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """EventCode=5137"""
  """A directory service object was created"""
]
Fields = [
  """({event_name}A directory service object was created)"""
  """({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
  """ComputerName =({host}[\w.\-]+)"""
  """EventCode=({event_code}\w+)"""
  """Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)"""
  """Object:.+?Class:\s+({ds_object_class}.+?)\s+Operation:"""
  """Object:\s+DN:\s+({ds_object_dn}.+?)\s+GUID:"""
  """Object:\s+DN:.+?({ds_object_ou}OU.+?)\s+GUID:"""
  """Directory Service:\s*Name(:|=)\s*({ds_name}[^\s]+)\s*.*?Type(:|=)\s*({ds_type}.*?Services)"""
  """GUID(:|=)\s*\{({object_id}[^\}]+)"""
  """Operation:\s*Correlation ID(:|=)\s*\{({correlation_id}[^\}]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```