#### Parser Content
```Java
{
Name = snort-s-json-alert-trigger-success-idssnort
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Snort
  Product = Snort
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"program":"snort"""", """"logT":"IDS-Snort"""", """[Classification:""" ]
  Fields = [
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.message,exa_regex=\[({additional_info}[^"\]]+)\] ({alert_name}.+?)\s*\[Classification:\s*({alert_type}[^\]]+)\] \[Priority:\s*({alert_severity}[^\]]+)\] \{({protocol}[^\}]+)\} ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({src_port}\d+) -> ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)""",
    ]


}
```