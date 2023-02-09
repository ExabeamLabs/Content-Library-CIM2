#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-userstopvm
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: USER_STOP_VM"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*? VM ({object}[^\s"]+) powered off by ({user}[^\s\(\)]+?) \(({resource}[^\)]+)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```