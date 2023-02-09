#### Parser Content
```Java
{
Name = vmware-esxi-str-app-activity-vpxd
  Vendor = VMware
  Product = VMware ESXi
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""] [""", """ vpxd """, """Event [""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)[^\s]+\s+({host}[^\s]+)\s""",
    """Event\s*(\[[^\]]*\]\s+){2}({additional_info}[^\]\}]+?)\s*$""",
    """Event\s*(\[[^\]]*\]\s+){8}\[({additional_info}[^\]]+?)\s*\]"""
  ]


}
```