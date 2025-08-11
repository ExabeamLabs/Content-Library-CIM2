#### Parser Content
```Java
{
Name = vectra-cd-json-alert-trigger-success-detection-1
  Vendor = Vectra
  Product = Vectra Cognito Detect
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"category":"""", """mitre""", """"detection_type":"""", """"d_type_vname"""" ]
  Fields = [
    """exa_json_path=$.event_timestamp,exa_field_name=time""",
    """exa_json_path=$.category,exa_field_name=alert_type""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.d_type_vname,exa_field_name=alert_subject""",
    """exa_json_path=$.detection_type,exa_field_name=alert_name""",
    """exa_json_path=$.detection_id,exa_field_name=alert_id""",
    """exa_json_path=$.detail.app_protocol,exa_field_name=app_protocol"""
    """exa_json_path=$.detail.target_domain,exa_field_name=dest_domain"""
    """exa_json_path=$.detail.dst_hosts.ip,exa_field_name=dest_ip""",
    """exa_json_path=$.detail.src_hosts.ip,exa_field_name=src_ip""",
    """exa_json_path=$.detail.src_hosts.name,exa_field_name=src_host""",
    """exa_json_path=$.detail.dst_ip,exa_field_name=dest_ip""",
    """exa_json_path=$.detail.dst_hosts.name,exa_field_name=dest_host""",
    """exa_json_path=$.entity_uid,exa_field_name=src_host""",
    """exa_json_path=$.detail.bytes_received,exa_field_name=bytes_in""",
    """exa_json_path=$.detail.bytes_sent,exa_field_name=bytes_out""",
    """exa_json_path=$.triaged,exa_field_name=additional_info""",
    """exa_json_path=$.mitre,exa_field_name=mitre_labels"""
    """exa_json_path=$.detail.dst_host.ip,exa_field_name=dest_ip"""
    """exa_json_path=$.detail.dst_host.name,exa_field_name=dest_host"""
    """exa_json_path=$.detail.dst_port,exa_field_name=dest_port"""
    """exa_json_path=$.category,exa_field_name=tactic"""
  ]
  ParserVersion = "v1.0.0"  


}
```