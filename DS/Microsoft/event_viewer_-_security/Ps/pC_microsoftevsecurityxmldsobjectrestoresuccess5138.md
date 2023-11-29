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
  """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))<"""
  """Security ID:\s+({user_sid}[^\s]+?)\s+Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Account Domain:\s+((?i)(NA)|({domain}[^\s]+?))\s+Logon ID:\s+({login_id}[^\s]+)"""
  """Class:\s+({object_class}[^:]+?)\s+Operation:"""
  """Object:[^\{\}]+?New DN:\s+({object_dn}[^\s]+)"""
  """Object:\s+Old DN:[^\{\}]+?({object_ou}OU[^\s]+?)\s+GUID:"""
  """Directory Service:\s*Name:\s*({service_name}[^\s]+)\s+Type:\s*({service_type}[^:]*?Services)"""
  """<Data Name\\*='ObjectGUID'>\{({guid}[^<\}]+)\}<"""
  """<Data Name\\*='OpCorrelationID'>\{({correlation_id}[^\}<]+)\}<"""
]
ParserVersion = "v1.0.0"


}
```