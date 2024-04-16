#### Parser Content
```Java
{
Name = "microsoft-365defender-json-alert-trigger-success-publish-1"
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"category":"AdvancedHunting-AlertInfo"""", """"operationName":"Publish"""", """"Severity":""", """"Title":""" ]
  Fields = [
    """exa_regex="Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"exa_json_path=$.hostname,exa_field_name=host""""
    """exa_json_path=$.AlertId,exa_field_name=alert_id"""
    """exa_json_path=$.Title,exa_field_name=alert_name"""
    """exa_json_path=$.ategory,exa_field_name=alert_type"""
    """exa_json_path=$.Severity,exa_field_name=alert_severity"""
    """exa_json_path=$.DetectionSource,exa_field_name=alert_source"""
  ]
  DupFields = [ "alert_name->alert_subject" ]
  ParserVersion = "v1.0.0"


}
```