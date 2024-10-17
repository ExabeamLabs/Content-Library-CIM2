#### Parser Content
```Java
{
Name = checkpoint-sg-kv-app-activity-awareness
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point Security Gateway
  TimeFormat = "epoch_sec"
  Conditions = [ """ CheckPoint """, """product:"""", """; description:"""", """product:"Identity Awareness"""" ]
  Fields = [
    """\Wtime(:|=)"({time}\d{10})""",
    """\W({host}[\w\-.]+)\s+CheckPoint""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """\Worigin_sic_name:"CN=({origin_name}[^",]+)""",
    """\Wproduct:"({product_name}[^"]+)""",
    """\Wdescription:"({event_name}[^"]+)""",
    """\Wsrc:"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst:"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]


}
```