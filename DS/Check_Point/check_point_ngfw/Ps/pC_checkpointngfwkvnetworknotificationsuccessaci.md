#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-network-notification-success-aci
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Conditions = [ """ CheckPoint """, """product:"ACI"""", """default_device_message:""", """syslog_severity:"""" ]
  Fields = [
    """\Wtime:"({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wsyslog_severity:"({alert_severity}[^"]+)"""",
    """\Worigin:"({origin_ip}[A-Fa-f\d\.:]+)"""",
    """\Wproduct:"({product_name}[^"]+)"""",
    """\Wifdir:"({direction}[^"]+)"""",
    """default_device_message:"[^%]+({additional_info}.+?)\s*";"""
  ]
  ParserVersion = v1.0.0


}
```