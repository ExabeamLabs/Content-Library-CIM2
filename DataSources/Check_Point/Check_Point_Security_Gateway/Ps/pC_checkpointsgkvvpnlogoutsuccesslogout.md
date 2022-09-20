#### Parser Content
```Java
{
Name = checkpoint-sg-kv-vpn-logout-success-logout
  ParserVersion = "v1.0.0"
  Vendor = Check Point
  Product = Check Point Security Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """ProductName: Connectra;""", """Action: logout;""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+((\+|\-)\d\d:\d\d)?)""",
    """({host}[\w.\-]+)\s+CPLogToSyslog:""",
    """\WOriginSicName:\s*CN=({host}[\w.\-]+),O="""
    """\WAction:\s*(|({action}[^;]+?));""",
    """\Wuser:\s*({full_name}.+?)\s*(\(({account}.+?))?(\)|;)"""
    """\Wsrc:\s*(|({src_ip}[a-fA-F\d.:]+));""",
    """\WProductName:\s*(|({app}[^;]+?));""",
    """\Whost_ip:\s*({dest_ip}[a-fA-F\d.:]+)""",
    """\Wassigned_IP::\s*({dest_ip}[a-fA-F\d.:]+)""",
  ]
   DupFields = [ "action->event_name", "full_name->user" ]


}
```