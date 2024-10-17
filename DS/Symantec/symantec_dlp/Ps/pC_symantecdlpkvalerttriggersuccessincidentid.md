#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-incidentid
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""INCIDENTID=""", """, blocked="""", """, policy="""", """, sender="""", """, severity=""""]
  Fields = [
    """detection_date="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """hostname="({src_host}[^"]+)"""",
    """INCIDENTID="({alert_id}\d+)"""",
    """severity="({alert_severity}\d+)"""",
    """policy="({alert_name}[^"]+)"""",
    """username="(({domain}[^\\"]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """domain="({domain}[^"]+)"""",
    """sender="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """recipients="({target}[^"@]+@[^"]+)"""",
    """subject="\s*({additional_info}[^"]+?)\s*"""",
    """blocked="({action}\d+)""""
  ]
  DupFields = [ "alert_name->alert_type"]
  ParserVersion = "v1.0.0"


}
```