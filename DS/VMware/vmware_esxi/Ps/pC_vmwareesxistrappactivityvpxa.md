#### Parser Content
```Java
{
Name = vmware-esxi-str-app-activity-vpxa
  Vendor = VMware
  Product = VMware ESXi
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""" Vpxa:""", """Originator@6876""", """ vpxa[""", """sub=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({host}[^\s]+)\sVpxa:""",
    """user=((({domain}[^\\\s@]+)\\+)?({user}[\w\.\-]{1,40}\$?))""",
    """Vpxa:\s+({additional_info}[^"]+?)\s*$"""
  ]


}
```