#### Parser Content
```Java
{
Name = symantec-endpointprotection-json-alert-trigger-success-80
  Vendor = Symantec
  Product = Symantec Advanced Threat Protection
  ParserVersion = "v1.0.0"
  Conditions = [ """"destinationServiceName":"Symantec"""", """"product_name":"Symantec """,""""type_id":80""",""""type":""" ]
  Fields = ${SymantecParsersTemplates.json-symantec-endpoint-protection.Fields}[
    """"actor":[^\}]+?"path":"({process_path}({process_dir}(?:[^";]+)?[\\\/;])?({process_name}[^\\\/";]+?))"""",
    """"actor":.+?"pid":({process_id}\d+)""",
    """"feature_name":"({alert_type}[^"]+)"""",
    """"policy":[^\}]+?"name":"({alert_name}[^"]+)""",
    """"severity_id":({alert_severity}\d+)""",
    """"type_id":({event_code}\d+)"""
  ]


}
```