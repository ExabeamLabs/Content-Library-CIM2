#### Parser Content
```Java
{
Name = vmware-esxi-str-endpoint-login-success-accepted
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """EMC VMWare""","""Login Succeeded""","""Accepted """, """ for user """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\d\d.\d\d\d\w\s(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))\sHostd:""",
    """\s+from\s+(::[\w]+:)?({src_ip}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|::1))"""
  ]
  ParserVersion = "v1.0.0"


}
```