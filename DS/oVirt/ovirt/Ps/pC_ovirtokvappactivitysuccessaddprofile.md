#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-addprofile
  Vendor = oVirt
  Product = oVirt
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """EVENT_ID: ADD_VNIC_PROFILE""", """ovirt""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt""",
    """EVENT_ID:\s*({operation}[^\(\)]+)""",
    """EVENT_ID:.*?\(User: ({user}[\w\.\-]{1,40}\$?)""",
    """({app}ovirt)"""
  ]
  ParserVersion = "v1.0.0"


}
```