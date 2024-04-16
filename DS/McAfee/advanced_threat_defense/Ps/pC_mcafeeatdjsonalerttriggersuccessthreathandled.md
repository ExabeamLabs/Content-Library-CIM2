#### Parser Content
```Java
{
Name = mcafee-atd-json-alert-trigger-success-threathandled
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = Advanced Threat Defense
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""""detecting_product_name":"MSME"""" , """threat_source_process_name""" , """threat_handled"""]
  Fields = [
    """exa_json_path=$.event_generated_time,exa_regex=^({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """exa_json_path=$.threat_source_user_name,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.threat_target_user_name,exa_field_name=target""",
    """exa_json_path=$.detecting_product_ip_address,exa_field_name=host""",
    """exa_json_path=$.detecting_product_host_name,exa_field_name=host""",
    """exa_json_path=$.threat_severity,exa_field_name=alert_severity""",
    """exa_json_path=$.event_category,exa_field_name=alert_type""",
    """exa_json_path=$.threat_source_process_name,exa_field_name=process_path""",
    """exa_json_path=$.action_taken,exa_field_name=result""",
    """exa_json_path=$.threat_type,exa_field_name=alert_name""",
  ]


}
```