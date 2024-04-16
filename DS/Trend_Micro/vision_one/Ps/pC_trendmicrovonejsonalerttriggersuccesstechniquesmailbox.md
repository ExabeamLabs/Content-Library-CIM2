#### Parser Content
```Java
{
Name = trendmicro-vone-json-alert-trigger-success-techniques-mailbox
  Vendor = Trend Micro
  Product = Vision One
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"techniques":""", """"tactics":""", """"level":""", """"filters":""", """"entityType":"mailbox"""" ]
  Fields = [
    """exa_json_path=$.entityType,exa_field_name=alert_type"""
    """exa_json_path=$.filters[0].description,exa_field_name=description"""
    """exa_json_path=$.filters[0].level,exa_field_name=alert_severity"""
    """exa_json_path=$.filters[0].name,exa_field_name=alert_name""" 
    """exa_json_path=$.detectionTime,exa_field_name=time"""
    """exa_json_path=$..highlightedObjects[?(@.type == 'user_account')].value,exa_field_name=email_address"""
    """exa_json_path=$..highlightedObjects[?(@.type == 'detection_name')].value,exa_field_name=rule"""
  ]


}
```