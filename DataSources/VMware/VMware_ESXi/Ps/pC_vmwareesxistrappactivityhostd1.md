#### Parser Content
```Java
{
Name = vmware-esxi-str-app-activity-hostd-1
  Vendor = VMware
  Product = VMware ESXi
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Hostd: """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({host}[^\s]+)\s""",
    """Hostd:\s*({additional_info}[^=]+?)\s*$"""
  ]


}
```