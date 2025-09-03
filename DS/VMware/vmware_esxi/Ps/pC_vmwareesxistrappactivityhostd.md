#### Parser Content
```Java
{
Name = vmware-esxi-str-app-activity-hostd
  Vendor = VMware
  Product = VMware ESXi
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""" Hostd:""", """Originator@6876""", """ hostd[""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({host}[^\s]+)\sHostd:""",
    """user=([^:\]]+:)?((({domain}[^\\\s@]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """Hostd:\s+({additional_info}[^"]+?)\s*$"""
    """user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]


}
```