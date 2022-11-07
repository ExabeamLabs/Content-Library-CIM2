#### Parser Content
```Java
{
Name = f5-silverline-kv-network-session-fail-irule
  ParserVersion = v1.0.0
  Product = F5 Silverline
  Vendor = F5
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ type=irule, """, """ log_type="irule", """, """ irule-version=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s+({host}\S+)\s+""",
    """\sclient_ip="+({src_ip}[A-Fa-f\d.-]+)"+""",
    """\sclient_port=({src_port}\d+)""",
    """\\"action\\":\\"({action}[^\\"]+)\\"""",
    """\sirule="({rule}[^"]+)"""",
    """\slog_type="({event_category}[^"]+)"""",
    """\sloglevel=({severity}\d+)""",
# proxy_id is removed
    """\sservice_id="({service_id}\d+)""",
    """\svirtualserver="({target_uri}[^"]+)"""",
    """\svs_ip="({dest_ip}[^"]+)"""",
  ]


}
```