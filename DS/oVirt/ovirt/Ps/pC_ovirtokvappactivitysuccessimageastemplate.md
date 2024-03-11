#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-imageastemplate
  Vendor = oVirt
  Product = oVirt
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """EVENT_ID: USER_IMPORT_IMAGE_AS_TEMPLATE""", """ovirt""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt""",
    """EVENT_ID:\s*({operation}[^\(\)]+)""",
    """EVENT_ID:.*?User ({user}[^\s\(\)"]+)""",
    """({app}ovirt)"""
  ]
  ParserVersion = "v1.0.0"


}
```