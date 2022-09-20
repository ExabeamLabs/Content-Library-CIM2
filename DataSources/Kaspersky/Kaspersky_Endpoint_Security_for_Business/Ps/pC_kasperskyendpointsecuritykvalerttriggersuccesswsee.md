#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-kv-alert-trigger-success-wsee
  ParserVersion = v1.0.0
  Vendor = Kaspersky
  Product = Kaspersky Endpoint Security for Business
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ WSEE|""", """ p2="""", """ p5="""",""" tdn="""", """ hdn="""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) ({host}[\w\-.]+) WSEE\|""",
    """hip="({src_ip}[A-Fa-f:\d.]+)""",
    """hdn="({src_host}[^"]+)""",
    """p2="({url}[^"]+)""",
    """p2="({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/"]+)+)?[\\\/]+)({process_name}[^"\\\/]+))""",
    """etdn="({alert_name}[^"]+)""",
    """p5="({alert_name}[^"]+)""",
    """tdn="({alert_type}[^"]+)""",
    """et="({alert_type}[^"]+)""",
    """p7="(({domain}[^"\\]+)\\+)?({user}[^\\\s"]+)""",
  ]


}
```