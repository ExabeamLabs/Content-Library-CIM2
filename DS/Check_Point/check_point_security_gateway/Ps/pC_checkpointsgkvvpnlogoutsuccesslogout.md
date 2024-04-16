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
    """\Wsrc:\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?);""",
    """\WProductName:\s*(|({app}[^;]+?));""",
    """\Whost_ip:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wassigned_IP::\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]
   DupFields = [ "action->event_name", "full_name->user" ]


}
```