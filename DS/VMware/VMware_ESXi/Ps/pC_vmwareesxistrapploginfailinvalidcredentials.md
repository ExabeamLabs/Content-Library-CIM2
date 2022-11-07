#### Parser Content
```Java
{
Name = vmware-esxi-str-app-login-fail-invalidcredentials
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""fdm[""", """Fdm:""",  """Invalid Credentials""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s({host}[\w.-]+)\s+Fdm:""",
    """(?i)IP\s+({src_ip}[A-Fa-f.:\d]+)""",
    """({failure_reason}Invalid Credentials)""",
    """Fdm:\s+({additional_info}[^\$]+?)\s*$"""
  ]


}
```