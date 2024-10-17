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
    """src_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """dest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """threat_type="(\s+|({alert_type}[^"]+))"""",
    """dest_nt_domain="({domain}[^"]+)"""",
    """user="*(N\/A|\s+|NULL|([^\\]+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """AutoID="({alert_id}[^"]+)""""
  ]


}
```