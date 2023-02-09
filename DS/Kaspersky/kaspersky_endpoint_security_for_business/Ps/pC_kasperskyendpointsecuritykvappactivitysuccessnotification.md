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
    """hip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """hdn="({src_host}[^"]+)""",
    """etdn="({alert_name}[^"]+)""",
    """et="({alert_type}[^"]+)""",
  ]


}
```