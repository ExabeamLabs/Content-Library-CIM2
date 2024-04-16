#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-endpoint
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""protocol=Endpoint""","""signature="""]
  Fields = [
    """,severity=({alert_severity}\d{1})""",
    """protocol=Endpoint\s({protocol}[^,]*),""",
    """dest_host=({target}.*?),incident""",
    """src_host=({src_host}[^,]*),subject""",
    """user=[^@]*@({domain}[^,]+)""",
    """event_id=({alert_id}\d{6})""",
    """signature=({alert_name}[^,]*)""",
    """subject=({additional_info}[^,]*)""",
    """protocol=({alert_type}[^,]*),""",
    """user=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)),"""
  ]
  ParserVersion = "v1.0.0"


}
```