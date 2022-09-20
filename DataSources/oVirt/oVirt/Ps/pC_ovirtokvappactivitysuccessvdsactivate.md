#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-vdsactivate
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: VDS_ACTIVATE"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*?User(:)? ({user}[^\s\(\)"]+?)(\)|\s|\.\s|\.$)"""
  """EVENT_ID:.*? Activation of host ({object}[^\s"]+) initiated by ({user}[^\s\(\)]+?)(\)|\s|\.\s|\.$)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```