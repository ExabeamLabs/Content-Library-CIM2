#### Parser Content
```Java
{
Name = vectra-cd-json-app-activity-success-hostscoring
  Vendor = Vectra
  Product = Vectra Cognito Detect
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"category":"HOST_SCORING"""", """detection_type""", """"severity"""", """is_prioritized""" ]
  Fields = [
    """exa_json_path=$.severity,exa_field_name=severity""",
    """exa_json_path=$.last_detection.type,exa_field_name=event_name""",
    """exa_json_path=$.event_timestamp,exa_field_name=time""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.is_prioritized,exa_field_name=additional_info""",
    """exa_json_path=$.name,exa_field_name=src_host"""
  ]
  DupFields = [ "category->operation"]
  ParserVersion = "v1.0.0"  


}
```