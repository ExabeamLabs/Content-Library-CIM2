#### Parser Content
```Java
{
Name = symantec-endpointprotection-json-alert-trigger-success-80
  ExtractionType = json
  Vendor = Symantec
  Product = Symantec Advanced Threat Protection
  ParserVersion = "v1.0.0"
  Conditions = [ """"product_name":"Symantec """,""""type_id":80""",""""type":""", """"severity_id":""" ]
  Fields = ${SymantecParsersTemplates-1.json-symantec-endpoint-protection.Fields}[
    """exa_json_path=$.feature_name,exa_field_name=alert_type"""
    """exa_json_path=$.policy.name,exa_field_name=alert_name"""
    """exa_json_path=$.severity_id,exa_field_name=alert_severity"""
    """exa_json_path=$.type_id,exa_field_name=event_code"""
  ]


}
```