#### Parser Content
```Java
{
Name = protectwise-ndr-kv-alert-trigger-success-protectwiseemitter
  Vendor = Verizon
  Product = Verizon NDR
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ protectwise-emitter[""" ]
  Fields = [
    """({time}\d{1,4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.[^\s.]+)""",
    """\d\d:\d\d:\d\d\s({host}[^=]+?).\s<""",
    """src\s-\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst\s-\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """classification:\s({alert_type}[^,]*)""",
    """description:\s({alert_name}[^,]*)""",
  ]


}
```