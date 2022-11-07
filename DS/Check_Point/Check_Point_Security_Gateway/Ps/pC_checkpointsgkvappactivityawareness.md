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
    """\Wtime:"({time}\d+)""",
    """\W({host}[\w\-.]+)\s+CheckPoint""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """\Worigin_sic_name:"CN=({origin_name}[^",]+)""",
    """\Wproduct:"({product_name}[^"]+)""",
    """\Wdescription:"({event_name}[^"]+)""",
    """\Wifdir:"({direction}[^"]+)""",
  ]


}
```