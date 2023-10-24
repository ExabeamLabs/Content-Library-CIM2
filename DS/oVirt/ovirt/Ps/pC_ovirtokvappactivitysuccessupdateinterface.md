#### Parser Content
```Java
{
Name = ovirt-o-kv-app-activity-success-updateinterface
  Vendor = oVirt
  Product = oVirt
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """EVENT_ID: NETWORK_UPDATE_VM_INTERFACE""", """ovirt""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt""",
    """EVENT_ID:\s*({operation}[^\(\)]+)""",
    """EVENT_ID:.*?Interface nic1 \(({resource}[^\)]+)\) was updated for VM ({object}[^\s"]+?)\.\s{1,100}\(User: ({user}[\w\.\-]{1,40}\$?)""",
    """({app}ovirt)"""
  ]
  ParserVersion = "v1.0.0"


}
```