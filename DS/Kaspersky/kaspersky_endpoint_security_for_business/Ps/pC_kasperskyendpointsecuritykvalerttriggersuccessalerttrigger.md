#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-kv-alert-trigger-success-alerttrigger
Vendor = Kaspersky
Product = Kaspersky Endpoint Security for Business
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """nId: """"
  """ EventDisplayName: """"
  """ wstrPar5: """"
]
Fields = [
  """DeviceTime:\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """hostname:\s*"({host}[^"]+)"""
  """nId:\s*"({alert_id}[^"]+)"""
  """EventDisplayName:\s*"({alert_name}[^"]+)"""
  """wstrPar5:\s*"(null|({alert_name}[^"]+))"""
  """wstrPar2:\s*"(null|({malware_url}[^"]+))"""
  """wstrPar8:\s*"(null|({alert_severity}[^"]+))"""
  """User:\s+(({domain}[^\\]*)\\+)?({user}[^\\\s]+)\s*\("""
  """\d+:\d+:\d+.+?({dest_ip}\d+\.\d+\.\d+\.\d+).*?nId:"""
]
DupFields = [
  "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```