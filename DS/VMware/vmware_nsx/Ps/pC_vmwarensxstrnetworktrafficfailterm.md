#### Parser Content
```Java
{
Name = vmware-nsx-str-network-traffic-fail-term
  Vendor = VMware
  Product = VMware NSX
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ INET""", """ TERM """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ({host}[\w\.\-]+)""",
    """\sINET\d* ({action}TERM)""",
    """({direction}IN|OUT)\s+({protocol}\w+)\s+(\S+\s+)?(\S+\s+)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({src_port}\d+))?->({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({dest_port}\d+))?\s+\S+\s+({bytes_in}\d+)\/({bytes_out}\d+)"""
  ]


}
```