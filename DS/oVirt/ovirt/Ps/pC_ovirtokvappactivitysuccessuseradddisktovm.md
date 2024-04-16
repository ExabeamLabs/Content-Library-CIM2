#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-useradddisktovm
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: USER_ADD_DISK_TO_VM"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*? Add-Disk operation of ({resource}[^\s]+) was initiated on VM ({object}[^\s"]+) by ({user}[\w\.\-]{1,40}\$?)(\)|\s|\.\s|\.$)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```