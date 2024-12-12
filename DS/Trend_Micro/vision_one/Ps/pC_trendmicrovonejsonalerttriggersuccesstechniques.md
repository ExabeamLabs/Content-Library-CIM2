#### Parser Content
```Java
{
Name = trendmicro-vone-json-alert-trigger-success-techniques
  Vendor = Trend Micro
  Product = Vision One
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"techniques":""", """"tactics":""", """"level":""", """"filter""", """highlightedObjects""" ]
  Fields = [
    """exa_json_path=$.entityType,exa_field_name=entity_type"""
    """exa_json_path=$.filters[0].description,exa_field_name=description"""
    """exa_json_path=$.filters[0].level,exa_field_name=alert_severity"""
    """exa_json_path=$.detectionTime,exa_field_name=time"""
    """exa_json_path=$.filters[0].name,exa_field_name=alert_name"""
    """exa_json_path=$.entityName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$..highlightedObjects[?(@.type == 'email_sender')].value,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$..highlightedObjects[?(@.type == 'email_subject')].value,exa_field_name=email_subject"""
    """exa_json_path=$..highlightedObjects[?(@.type == 'email_message_id')].value,exa_regex=\<({message_id}[^"\>]+)"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.description,exa_field_name=description"""
    """exa_json_path=$.filter.name,exa_field_name=alert_name"""
  ]


}
```