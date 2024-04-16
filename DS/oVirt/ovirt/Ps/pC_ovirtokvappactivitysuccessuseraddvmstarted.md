#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-useraddvmstarted
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: USER_ADD_VM_STARTED"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*?User(:)? ({user}[\w\.\-]{1,40}\$?)(\)|\s|\.\s|\.$)"""
  """EVENT_ID:.*? VM ({object}[^\s"]+) creation was initiated by ({user}[\w\.\-]{1,40}\$?)(\)|\s|\.\s|\.$)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```