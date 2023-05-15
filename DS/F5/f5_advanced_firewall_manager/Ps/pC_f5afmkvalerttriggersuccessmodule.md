#### Parser Content
```Java
{
Name = f5-afm-kv-alert-trigger-success-module
  Vendor = F5
  Product = F5 Advanced Firewall Manager
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """device_vendor="F5"""", """device_product="Advanced Firewall Module"""", """dos_attack_name=""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}(\+|-)\d{2}:\d{2})\s({host}[\w.-]+)""",
    """dos_attack_name="({alert_name}[^"]+)"""",
    """\Werrdefs_msg_name="({event_name}[^"]+)""",
    """severity="({alert_severity}[^"]+)""""
  ]


}
```