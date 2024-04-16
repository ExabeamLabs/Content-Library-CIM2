#### Parser Content
```Java
{
Name = vmware-esxi-str-app-notification-lookingfordc
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = ["""lwsmd:""", """Looking for a DC in domain""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s({host}[\w.-]+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s({host}[\w.-]+)\s""",
    """domain\s'(<(?i)null>|({domain}[^',]+))""",
    """\[[^\]]+?\]\s+({additional_info}\w+\s.*?)\s*("|$)"""
# flag is removed
  ]


}
```