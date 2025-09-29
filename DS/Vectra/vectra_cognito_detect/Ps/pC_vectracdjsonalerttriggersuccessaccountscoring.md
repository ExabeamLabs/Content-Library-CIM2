#### Parser Content
```Java
{
Name = vectra-cd-json-alert-trigger-success-accountscoring
  Vendor = Vectra
  Product = Vectra Cognito Detect
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"category":"ACCOUNT SCORING"""", """detection_type""", """"severity"""", """is_prioritized""" ]
  Fields = [
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.last_detection.type,exa_field_name=alert_name""",
    """exa_json_path=$.event_timestamp,exa_field_name=time""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.is_prioritized,exa_field_name=additional_info""",
    """exa_json_path=$.name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,]+))?))"""
    """exa_json_path=$.urgency_score,exa_field_name=risk_score""",
  ]
  DupFields = [ "category->operation","alert_name->alert_type"]
  ParserVersion = "v1.0.0"  


}
```