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
    """(?i)IP\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({failure_reason}Invalid Credentials)""",
    """Fdm:\s+({additional_info}[^\$]+?)\s*$"""
  ]


}
```