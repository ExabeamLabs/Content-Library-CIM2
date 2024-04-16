#### Parser Content
```Java
{
Name = "tanium-cp-json-alert-trigger-success-eventtrace"
  ExtractionType = json
  Vendor = "Tanium"
  Product = "Tanium Core Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """tanium-trace"""
    """Timestamp"""
    """Computer Name"""
    """Computer IP"""
  ] 
  Fields = [
    """exa_json_path=$.['Event Id'],exa_field_name=alert_id"""
    """exa_json_path=$.Timestamp,exa_field_name=time"""
    """exa_json_path=$.['User Name'],exa_field_name=user"""
    """exa_json_path=$.['User Id'],exa_field_name=user"""
    """exa_json_path=$.['User Domain'],exa_field_name=domain"""
    """exa_json_path=$.Severity,exa_field_name=alert_severity"""
    """exa_json_path=$.Priority,exa_field_name=alert_severity"""
    """exa_json_path=$.['Event Name'],exa_field_name=alert_name"""
    """exa_json_path=$.['Event Name'],exa_field_name=alert_type"""
    """exa_json_path=$.['Computer Name'],exa_field_name=src_host"""
    """exa_regex="fullpath\\?":\\?"({malware_url}[^"]+)\\*"""
    """exa_json_path=$.['Other Parameters'],exa_regex="type\\":\\"({alert_type}[^"]+?)\\*""""
    """exa_json_path=$.['Other Parameters'],exa_regex="name\\":\\"({file_name}[^"]+?)\\*""""
    """exa_regex="source\\":\\"({log_source}[^"\\]+)\\*""""
    """exa_json_path=$.['Computer IP'],exa_field_name=src_ip"""
  ]
  ParserVersion = "v1.0.0"


}
```