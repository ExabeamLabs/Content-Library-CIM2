#### Parser Content
```Java
{
Name = vmware-esxi-str-app-notification-lookingfordc
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = ["""lwsmd:""", """Looking for a DC in domain""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s({host}[\w.-]+)""",
    """domain\s'(<(?i)null>|({domain}[^']+))""",
# flag is removed
  ]


}
```