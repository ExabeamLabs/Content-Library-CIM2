#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-userstoppedvm
  Vendor = oVirt
  Product = oVirt
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """EVENT_ID: USER_STOPPED_VM_INSTEAD_OF_SHUTDOWN""", """ovirt""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt""",
    """EVENT_ID:\s*({operation}[^\(\)]+)""",
    """EVENT_ID:.*?User(:)? ({user}[^\s\(\)"]+?)(\)|\s|\.\s|\.$)""",
    """EVENT_ID:.*? VM ({object}[^\s"]+) was powered off ungracefully by ({user}[^\s\(\)]+) \(Host: ({resource}[^\)]+)""",
    """({app}ovirt)"""
  ]
  ParserVersion = "v1.0.0"


}
```