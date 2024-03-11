#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-userfailedrunvm
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: USER_FAILED_RUN_VM"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*? Failed to run VM ({object}[^\s"]+).*?The following disks are locked: ({resource}[^\s]+?)\.\s.*?\(User: ({user}[^\s\(\)"]+)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```