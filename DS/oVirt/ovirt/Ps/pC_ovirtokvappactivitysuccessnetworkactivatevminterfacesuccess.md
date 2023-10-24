#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-networkactivatevminterfacesuccess
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: NETWORK_ACTIVATE_VM_INTERFACE_SUCCESS"""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """EVENT_ID:\s*({operation}[^\(\)]+)"""
  """EVENT_ID:.*? was plugged to VM ({object}[^\s"]+?)\.?\s\(User: ({user}[\w\.\-]{1,40}\$?)(\)|\s|\.\s|\.$)"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```