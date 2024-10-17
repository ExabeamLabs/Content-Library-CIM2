#### Parser Content
```Java
{
Name = vmware-vcenter-str-user-password-modify-success-passwordwaschanged
  Vendor = VMware
  Product = vCenter
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ vcenter-server """, """ Password was changed """, """ on host """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s+({host}[\w\-.]+)\s""",
    """({service_name}vcenter-server)""",
    """\s({event_name}Password was changed) for account ({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\s({user}[\w\.\-\!\#\^\~]{1,40}\$?) account ({event_name}password was changed)""",
    """\son host ({src_host}[\w\-.]+)"""
  ]
  DupFields = [ "event_name->result" ]
  ParserVersion = "v1.0.0"


}
```