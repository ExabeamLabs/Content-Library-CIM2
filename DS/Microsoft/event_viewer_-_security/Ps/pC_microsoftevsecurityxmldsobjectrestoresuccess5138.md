#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-restore-success-5138"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>5138<"""
  """<Provider Name ="""
]
Fields = [
  """({event_name}A directory service object was undeleted)"""
  """({event_code}5138)"""
  """<Computer>({host}[^<]+)<"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))<"""
  """Security ID:\s+({user_sid}[^\s]+?)\s+Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+((?i)(NA)|({domain}[^\s]+?))\s+Logon ID:\s+({login_id}[^\s]+)"""
  """Class:\s+({object_type}[^:]+?)\s+Operation:"""
  """Object:[^\{\}]+?New DN:\s+({new_attribute}({ds_object_dn}.+?))\s+GUID:"""
  """Object:\s+Old DN:\s*({old_attribute}[^\{\}]+?({ds_object_ou}OU[^\s]+?)?)\s+New DN:"""
  """Object:\s+Old DN:[^\{\}]+?({ds_object_ou}OU[^\s]+?)\s+GUID:"""
  """Directory Service:\s*Name:\s*({ds_name}[^\s]+)\s+Type:\s*({ds_type}[^:]*?Services)"""
  """<Data Name\\*=('|")ObjectGUID('|")>\{({object_id}[^<\}]+)\}<"""
  """<Data Name\\*=('|")OpCorrelationID('|")>\{({correlation_id}[^\}<]+)\}<"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```