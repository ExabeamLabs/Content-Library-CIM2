#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-move-success-serviceobject"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
Conditions = [ """Directory Service:""", """Object:""", """Old DN:""", """New DN:""", """A directory service object was moved""" ]
Fields = [
  """({event_name}A directory service object was moved)""",
  """\d\d:\d\d:\d\d\s+({host}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(Microsoft-Windows-Security-Auditing|MSWinEventLog)""",
  """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
  """\s(Mon|Tue|Wed|Thu|Fri|Sat|Sun)\s({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d{4})\s""",
  """Security ID:\s+({user_sid}[^\s]+?)\s+Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Account Domain:\s+((?i)(NA)|({domain}[^\s]+?))\s+Logon ID:\s+({login_id}[^\s]+)""",
  """Class:\s+({ds_object_class}[^:]+?)\s+Operation:""",
  """Object:[^\{\}]+?New DN:\s+({ds_object_dn}[^:]+?)\s+GUID:""",
  """Object:\s+Old DN:[^\{\}]+?({src_ds_object_ou}OU[^:]+?)\s+GUID:""",
  """Directory Service:\s*Name:\s*({ds_name}[^\s]+)\s+Type:\s*({ds_type}[^:]*?Services)""",
  """GUID:\s*\{({guid}[^\}]+)""",
  """Operation:\s*Correlation ID:\s*\{({correlation_id}[^\}]+)""",
  """Object:\s+Old DN:[^\{\}]+?\s*({old_attribute}[^:]+?)\s+New DN:\s*({new_attribute}[^:]+?)\s+GUID:""",
  """({event_code}5139)"""
]
ParserVersion = "v1.0.0"


}
```