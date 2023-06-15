#### Parser Content
```Java
{
Name = symantec-edr-json-alert-trigger-success-8015
  ParserVersion = v1.0.0
  Conditions = [ """"destinationServiceName":"Symantec"""", """"product_name":"Symantec Endpoint Security"""", """"event_data_type":"fdr"""",""""type_id":8015""" ]
  Fields = ${SymantecParserTemplates.symantec-parser-template.Fields}[
    """"severity_id":({alert_severity}\d+)""",
    """"rule_name":"({alert_name}[^"]+)""",
    """"type_id":({event_code}8015)"""
  ]
  DupFields = [ "alert_name->alert_type" ]

symantec-parser-template = {
    Vendor = Symantec
    Product = Symantec Advanced Threat Protection
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"device_domain":"({domain}[^"]+)"""",
      """"device_name":"({src_host}[\w\-.]+)"""",
      """"device_os_name":"({os}[^"]+)"""",
      """"ipv4":\[?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"user_name":"({user}[^"]+)"""",
      """"rule_description":"({additional_info}[^"]+?)\s*"""",
    
}
```