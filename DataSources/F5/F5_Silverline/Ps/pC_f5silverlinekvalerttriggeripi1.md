#### Parser Content
```Java
{
Name = f5-silverline-kv-alert-trigger-ipi-1
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Silverline
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """type = ipi,""", """, errdefs_msg_name=IP""", """Intelligence Event,""", """, ip_intelligence_threat_name=""" ]
  Fields = [
    """date_time=({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    # """attack_type=({rule_type}[^,]+)""",
    """severity=({alert_severity}[^,]+)""",
    """action=({action}[^,]+)""",
    """dest_ip=({dest_ip}[a-fA-F\d\.:]+)?,""",
    """dest_port=({dest_port}\d+)?,""",
    """ip_protocol=({protocol}[^,]+),""",
    """source_ip=({src_ip}[a-fA-F\d\.:]+),""",
    """source_port=({src_port}\d+)""",
    """attack_type=({alert_type}[^\",]+)"""
  ]


}
```