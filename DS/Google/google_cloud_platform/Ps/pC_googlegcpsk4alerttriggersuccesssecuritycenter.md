#### Parser Content
```Java
{
Name = google-gcp-sk4-alert-trigger-success-securitycenter
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Cloud Platform 
  TimeFormat = "epoch_sec"
  Conditions = [ """finding_class:""", """resource_name:""", """category:""", """"security"""", """security_marks"""]
  Fields = [
    """event_time\s*\{.+?seconds:\s*({time}\d{10})""",
    """category:\s*"({alert_name}[^"]+)""",
    """finding_class:\s*({alert_type}[^\s\\]+)""",
    """severity:\s*({alert_severity}[^\s\\]+)""",
    """resource_name:\s*"({resource}[^"]+)""",
    """external_uri:\s*"({url}}[^"]+)""",
    """37:\s*"({additional_info}[^"]+)"""",
    """"security".+?1:\s*\{.+?"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  ]
  DupFields = [ "alert_name->event_name", "resource->object"] 


}
```