#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-userstartedvm
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: USER_STARTED_VM"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*? VM ({object}[^\s"]+) was started by ({user}[\w\.\-]{1,40}\$?) \(Host: ({resource}[^\)]+)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```