#### Parser Content
```Java
{
Name = f5-vip-str-alert-trigger-monitorstatus
  ParserVersion = v1.0.0
  Vendor = F5
  Product = BIG-IP F5 LBR
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss"]
  Conditions = [ """ notice mcpd[""", """: Pool """, """ monitor status """ ]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)([^\/]+?): Pool [^\s]+?\/([^\s]+)""",
    """\w+\s+\d{1,2}:\d{1,2}:\d{1,2}\s+({host}[^\s]+)\s*""",
    """: Pool \/[^\s]+([^:]+)\/(({dest_ip}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))|({dest_host}[^:]+)):(\d+) monitor status ({action}\w+)""",
# DL Fields are removed
# down_time is removed
# up_time is removed
  ]


}
```