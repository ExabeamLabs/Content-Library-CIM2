#### Parser Content
```Java
{
Name = mcafee-es-kv-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """signature_id="""", """threat_handled="""", """threat_type="""", """detection_method="""", """product="McAfee Endpoint Security"""" ]
  Fields = [
    """detected_timestamp="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """signature="(_|\s+|({alert_name}[^"]+))"""",
    """signature_id="({signature_id}[^"]+)"""",
    """category="({threat_category}[^"]+)"""",
    """fqdn="({host}[\w\-.]+)"""",
    """severity_id="({alert_severity}\d+)"""",
    """src_ip="({src_ip}[A-Fa-f0-9.:]+)"""",
    """dest_ip="({dest_ip}[A-Fa-f0-9.:]+)"""",
    """threat_type="(\s+|({alert_type}[^"]+))"""",
    """dest_nt_domain="({domain}[^"]+)"""",
    """user="*(N\/A|\s+|NULL|([^\\]+\\+)?({user}[^\s,"]+))"""",
    """AutoID="({alert_id}[^"]+)""""
  ]


}
```