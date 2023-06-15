#### Parser Content
```Java
{
Name = vmware-nsx-str-network-traffic-success-matchpass
  Vendor = VMware
  Product = VMware NSX
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ INET""", """ match PASS """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ({host}[\w\.\-]+)""",
    """\sINET\d* ({operation}match) ({result}PASS)""",
    """({direction}IN|OUT)\s+(\S+\s+)?({protocol}\w+) (\S+\s+)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({src_port}\d+))?->({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({dest_port}\d+))?"""
  ]


}
```