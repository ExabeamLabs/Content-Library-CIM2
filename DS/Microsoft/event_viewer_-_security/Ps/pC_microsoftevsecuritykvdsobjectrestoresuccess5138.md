#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-restore-success-5138"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Object:"""
  """Old DN:"""
  """New DN:"""
  """Directory Service:"""
  """A directory service object was undeleted"""
]
Fields = [
  """({event_name}A directory service object was undeleted)"""
  """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+Microsoft-Windows-Security-Auditing"""
  """Security ID:\s+({user_sid}[^\s]+?)\s+Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Account Domain:\s+((?i)(NA)|({domain}[^\s]+?))\s+Logon ID:\s+({login_id}[^\s]+)"""
  """Class:\s+({ds_object_class}[^:]+?)\s+Operation:"""
  """Object:[^\{\}]+?New DN:\s+({new_attribute}({ds_object_dn}[^\s]+))"""
  """Object:\s+Old DN:\s*({old_attribute}[^\{\}]+?({ds_object_ou}OU[^\s]+?)?)\s+New DN:"""
  """Object:\s+Old DN:[^\{\}]+?({ds_object_ou}OU[^\s]+?)\s+GUID:"""
  """Directory Service:\s*Name:\s*({ds_name}[^\s]+)\s+Type:\s*({ds_type}[^:]*?Services)"""
  """GUID:\s*\{({guid}[^\}]+)"""
  """Operation:\s*Correlation ID:\s*\{({correlation_id}[^\}]+)"""
  """\d\d:\d\d:\d\d\s+(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))\s+Microsoft-Windows-Security-Auditing"""
]
ParserVersion = "v1.0.0"


}
```