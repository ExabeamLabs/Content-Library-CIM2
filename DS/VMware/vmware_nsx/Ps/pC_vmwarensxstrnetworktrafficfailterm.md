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
    """({direction}IN|OUT)\s+({protocol}\w+)\s+(\S+\s+)?(\S+\s+)?({src_ip}[a-fA-F\d.:]+)(\/({src_port}\d+))?->({dest_ip}[a-fA-F\d.:]+)(\/({dest_port}\d+))?\s+\S+\s+({bytes_in}\d+)\/({bytes_out}\d+)"""
  ]


}
```