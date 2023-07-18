#### Parser Content
```Java
{
Name = vmware-esxi-str-http-session-fail-iofiltervpd
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""iofiltervpd""", """IOFVPSSL_VerifySSLCertificate:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)((\.\d+)?Z)\s({host}[\w.-]+)""",
    """({additional_info}({event_name}IOFVPSSL_VerifySSLCertificate)[^=]+?)\s*$"""
  ]


}
```