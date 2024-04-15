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
  """Security ID:\s+({user_sid}[^\s]+?)\s+Account Name:\s+({user}[^\s]+?)\s+Account Domain:\s+((?i)(NA)|({domain}[^\s]+?))\s+Logon ID:\s+({login_id}[^\s]+)"""
  """Class:\s+({object_class}[^:]+?)\s+Operation:"""
  """Object:[^\{\}]+?New DN:\s+({object_dn}[^\s]+)"""
   """Object:\s+Old DN:[^\{\}]+?({object_ou}OU[^\s]+?)\s+GUID:"""
  """Directory Service:\s*Name:\s*({service_name}[^\s]+)\s+Type:\s*({service_type}[^:]*?Services)"""
  """GUID:\s*\{({guid}[^\}]+)"""
  """Operation:\s*Correlation ID:\s*\{({correlation_id}[^\}]+)"""
  """\d\d:\d\d:\d\d\s+(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^<]+))\s+Microsoft-Windows-Security-Auditing"""
]
ParserVersion = "v1.0.0"


}
```