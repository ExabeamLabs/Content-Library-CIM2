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
    """Accepted ({auth}\S+) for user ({user}[^\s]+)""",
    """\s+from\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```