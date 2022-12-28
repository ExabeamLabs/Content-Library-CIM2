#### Parser Content
```Java
{
Name = vmware-carbonblack-json-app-notification-cbdefense
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = Carbon Black CES
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CB Defense""", """"EventID":7036""" ]
  Fields = [
    """Hostname":"({host}[^"]+)"""
    """EventReceivedTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
    """EventID":({event_code}[^,]+)"""
    """Message":"({operation}[^"]+)"""
    """Severity":"({severity}[^"]+)"""
    """ProcessID":({process_id}[^,]+)"""
    ]


}
```