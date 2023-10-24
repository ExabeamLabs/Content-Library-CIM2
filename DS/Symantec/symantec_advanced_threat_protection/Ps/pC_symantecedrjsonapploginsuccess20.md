#### Parser Content
```Java
{
Name = symantec-edr-json-app-login-success-20
  Vendor = Symantec
  Product = Symantec Advanced Threat Protection
  ParserVersion = "v1.0.0"
  Conditions = [ """"destinationServiceName":"Symantec"""", """"event_data_type":"sep"""",""""type_id":20""" ]
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