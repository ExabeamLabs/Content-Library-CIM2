#### Parser Content
```Java
{
Name = ovirt-kv-str-app-activity-success-templatefinishedsuccess
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: USER_IMPORT_IMAGE_AS_TEMPLATE_FINISHED_SUCCESS"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*?User ({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```