#### Parser Content
```Java
{
Name = symantec-endpointprotection-json-alert-trigger-success-8027-1
  ExtractionType = json
  Vendor = Symantec
  Product = Symantec Advanced Threat Protection
  ParserVersion = "v1.0.0"
  Conditions = [ """"product_name":"Symantec Endpoint """,""""type_id":8027""",""""type":"HOST_PROCESS_DETECTION"""" ]
  Fields = ${SymantecParsersTemplates-1.json-symantec-endpoint-protection-1.Fields}[
    """exa_json_path=$.policy.name,exa_field_name=alert_name"""
    """exa_json_path=$.severity_id,exa_field_name=alert_severity"""
    """exa_json_path=$.type_id,exa_field_name=event_code"""
    """exa_json_path=$.feature_name,exa_field_name=alert_type"""
  ]


}
```