#### Parser Content
```Java
{
Name = trendmicro-vone-json-alert-trigger-success-techniques-endpoint
  Vendor = Trend Micro
  Product = Vision One
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"techniques":""", """"tactics":""", """"level":""", """"filter""", """"entityType":""", """"endpoint",""" ]
  Fields = [
    """exa_json_path=$.entityType,exa_field_name=alert_type"""
    """exa_json_path=$.filters[0].description,exa_field_name=description"""
    """exa_json_path=$.filters[0].level,exa_field_name=alert_severity"""
    """exa_json_path=$.filters[0].name,exa_field_name=alert_name"""
    """exa_json_path=$.detectionTime,exa_field_name=time"""
    """exa_json_path=$.entityName,exa_regex=({src_host}[^"@(]+?)\("""
    """exa_json_path=$..highlightedObjects[?(@.type == 'command_line')].value,exa_field_name=process_command_line"""
    """exa_json_path=$..highlightedObjects[?(@.type == 'windows_event_log_id')].value,exa_field_name=event_code"""
    """exa_json_path=$..highlightedObjects[?(@.field == 'processName')].value,exa_regex=^({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))$"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.description,exa_field_name=description"""
    """exa_json_path=$.filter.name,exa_field_name=alert_name"""
  ]


}
```