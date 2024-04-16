#### Parser Content
```Java
{
Name = symantec-edr-json-app-login-success-20
  ExtractionType = json
  Vendor = Symantec
  Product = Symantec Advanced Threat Protection
  ParserVersion = "v1.0.0"
  Conditions = [ """"severity_id":""", """"event_id":""", """"event_data_type":"sep"""",""""type_id":20""" ]
  Fields = ${SymantecParsersTemplates-1.json-symantec-endpoint-protection.Fields}[
    """exa_json_path=$.severity_id,exa_field_name=alert_severity"""
    """exa_json_path=$.type_id,exa_field_name=event_code"""
  ]


}
```