#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-updatecluster
  Vendor = oVirt
  Product = oVirt
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """EVENT_ID: USER_UPDATE_CLUSTER""", """ovirt""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt""",
    """EVENT_ID:\s*({operation}[^\(\)]+)""",
    """EVENT_ID:.*? Host cluster ({object}[^\s"]+) was updated by ({user}[\w\.\-]{1,40}\$?)(\)|\s|\.\s|\.$)""",
    """({app}ovirt)"""
  ]
  ParserVersion = "v1.0.0"


}
```