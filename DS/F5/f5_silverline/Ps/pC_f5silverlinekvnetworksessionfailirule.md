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
    """\sclient_ip="+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+""",
    """\sclient_port=({src_port}\d+)""",
    """\\"action\\":\\"({action}[^\\"]+)\\"""",
    """\sirule="({rule}[^"]+)"""",
    """\slog_type="({event_category}[^"]+)"""",
    """\sloglevel=({severity}\d+)""",
# proxy_id is removed
    """\sservice_id="({service_id}\d+)""",
    """\svirtualserver="({target_uri}[^"]+)"""",
    """\svs_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
  ]


}
```