#### Parser Content
```Java
{
Name = suricata-s-json-alert-trigger-success-suricata
  ExtractionType = json
  Vendor = Suricata
  Product = Suricata
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"alert"""", """"event_source":"suricata"""", """"event_type":"alert""""]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.alert.signature,exa_field_name=alert_name"""
    """exa_json_path=$.alert.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.alert.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.event_type,exa_field_name=alert_type"""
    """exa_json_path=$.dest_ip,exa_field_name=dest_ip"""
    """exa_json_path=$.dest_port,exa_field_name=dest_port"""
    """exa_json_path=$.alert.signature_id,exa_field_name=alert_id"""
    """exa_json_path=$.proto,exa_field_name=protocol"""
    """exa_json_path=$.payload,exa_field_name=additional_info"""
    """exa_json_path=$.bricata.sensor_hostname,exa_field_name=src_host"""
    """exa_json_path=$.src_ip,exa_field_name=src_ip"""
  ]


}
```