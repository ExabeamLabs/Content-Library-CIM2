#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-kv-alert-trigger-success-kes
  ParserVersion = v1.0.0
  Vendor = Kaspersky
  Product = Kaspersky Endpoint Security for Business
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ KES|""", """ p2="""", """ p5="""",""" tdn="""", """ hdn="""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) ({host}[\w\-.]+) KES\|""",
    """hip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """hdn="({src_host}[^"]+)""",
    """p2="({malware_url}[^"]+)""",
    """p2="({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/"]+)+)?[\\\/]+)({process_name}[^"\\\/]+))""",
    """etdn="({alert_name}[^"]+)""",
    """p5="({alert_name}[^"]+)""",
    """tdn="({alert_type}[^"]+)""",
    """et="({alert_type}[^"]+)""",
    """p7="(({domain}[^"\\]+)\\+)?({user}[^\\\s"]+)""",
  ]


}
```