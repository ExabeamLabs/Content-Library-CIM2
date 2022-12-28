#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-vmsetticket
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: VM_SET_TICKET"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*?User ({user}[^\s\(\)"]+) initiated console session for VM ({object}[^\s"]+)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```