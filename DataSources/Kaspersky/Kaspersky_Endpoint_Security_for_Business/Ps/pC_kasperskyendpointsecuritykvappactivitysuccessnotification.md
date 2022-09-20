#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-kv-app-activity-success-notification
  Vendor = Kaspersky
  Product = Kaspersky Endpoint Security for Business
  ParserVersion = v1.0.0
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"GNRL_EV_FULLSCAN_STATUS_NOTIFICATION"""", """ WSEE|""", """ p1="""", """ hdn="""", """etdn="""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) ({host}[\w\-.]+) WSEE\|""",
    """hip="({src_ip}[A-Fa-f:\d.]+)""",
    """hdn="({src_host}[^"]+)""",
    """etdn="({alert_name}[^"]+)""",
    """et="({alert_type}[^"]+)""",
  ]


}
```