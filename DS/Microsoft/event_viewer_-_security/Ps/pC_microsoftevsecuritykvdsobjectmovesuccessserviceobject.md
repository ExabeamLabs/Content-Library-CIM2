#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-move-success-serviceobject"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [ """Directory Service:""", """Object:""", """Old DN:""", """New DN:""", """A directory service object was moved""" ]
Fields = [
  """({event_name}A directory service object was moved)""",
  """\d\d:\d\d:\d\d\s+({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s+(Microsoft-Windows-Security-Auditing|MSWinEventLog)""",
  """\s(Mon|Tue|Wed|Thu|Fri|Sat|Sun)\s({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d{4})\s""",
  """Security ID:\s+({user_sid}[^\s]+?)\s+Account Name:\s+({user}[^\s]+?)\s+Account Domain:\s+((?i)(NA)|({domain}[^\s]+?))\s+Logon ID:\s+({login_id}[^\s]+)""",
  """Class:\s+({ds_object_class}[^:]+?)\s+Operation:""",
  """Object:[^\{\}]+?New DN:\s+({src_ds_object_dn}[^:]+?)\s+GUID:""",
  """Object:\s+Old DN:[^\{\}]+?({src_ds_object_ou}OU[^:]+?)\s+GUID:""",
  """Directory Service:\s*Name:\s*({service_name}[^\s]+)\s+Type:\s*({service_type}[^:]*?Services)""",
  """GUID:\s*\{({guid}[^\}]+)""",
  """Operation:\s*Correlation ID:\s*\{({correlation_id}[^\}]+)""",
  """Object:\s+Old DN:[^\{\}]+?\s*({old_attribute}[^:]+?)\s+New DN:\s*({new_attribute}[^:]+?)\s+GUID:""",
  """({event_code}5139)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```