#### Parser Content
```Java
{
Name = extrahop-revealx-json-alert-trigger-success-detection
  Vendor = Extrahop
  Product = Extrahop Reveal(x)
  TimeFormat = "yyyy/MM/dd HH:mm:ss.SSS"
  ExtractionType = json
  Conditions = [ """"detectionType"""", """"event":"Detection"""", """"title":"""", """"riskScore":"""]
  Fields = [
    """exa_json_path=$.startTime,exa_field_name=time""",
    """exa_json_path=$.id,exa_field_name=alert_id""",
    """exa_json_path=$.title,exa_field_name=alert_name""",
    """exa_json_path=$.event,exa_field_name=alert_type""",
    """exa_json_path=$.riskScore,exa_field_name=original_risk_score""",
    """exa_json_path=$.offenders,exa_regex=\["({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """exa_json_path=$.victims,exa_regex=\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",    
    """exa_json_path=$.description,exa_field_name=additional_info"""
  ]
        DupFields = [ "original_risk_score->alert_severity"]
  ParserVersion = "v1.0.0"


}
```