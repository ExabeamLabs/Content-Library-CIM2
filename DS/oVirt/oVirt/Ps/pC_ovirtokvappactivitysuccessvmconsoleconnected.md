#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-vmconsoleconnected
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: VM_CONSOLE_CONNECTED"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*?User ({user}[^\s\(\)"]+) is connected to VM ({object}[^\s"]+)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```