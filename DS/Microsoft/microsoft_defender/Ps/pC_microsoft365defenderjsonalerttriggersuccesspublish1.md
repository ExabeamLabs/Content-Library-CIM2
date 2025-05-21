#### Parser Content
```Java
{
Name = "microsoft-365defender-json-alert-trigger-success-publish-1"
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"category":"AdvancedHunting-AlertInfo"""", """"operationName":"Publish"""", """"Severity":""", """"Title":""" ]
  Fields = [
    """exa_regex="Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"exa_json_path=$.hostname,exa_field_name=host""""
    """exa_json_path=$..AlertId,exa_field_name=alert_id"""
    """exa_json_path=$.category,exa_field_name=alert_type"""
    """exa_json_path=$..Severity,exa_field_name=alert_severity"""
    """exa_json_path=$..DetectionSource,exa_field_name=alert_source"""
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"hostname":"({host}[^"]+)"""",
    """"AlertId":"({alert_id}[^"]+)"""",
    """"Title":"({alert_subject}[^"]+?)(\\u200b)?"""",
    """exa_regex="Title":"({alert_subject}[^"]+?)(\\u200b)?"""",
    """"Title":"({alert_name}[^"\(]+?)(\s*\(|(\\u200b)?")""",
    """exa_regex="Title":"({alert_name}[^"\(]+?)(\s*\(|(\\u200b)?")""",
    """"(C|c)ategory":"({alert_type}[^"]+)"""",
    """"Severity":"({alert_severity}[^"]+)"""",
    """"DetectionSource":"({alert_source}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```