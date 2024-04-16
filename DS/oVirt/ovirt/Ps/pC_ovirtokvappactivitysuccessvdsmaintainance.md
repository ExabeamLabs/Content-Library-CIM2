#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-vdsmaintainance
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: USER_VDS_MAINTENANCE_WITHOUT_REASON"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*? Host ({object}[^\s"]+) was switched to Maintenance mode by ({user}[\w\.\-]{1,40}\$?)(\)|\s|\.\s|\.$)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```