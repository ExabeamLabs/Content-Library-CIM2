#### Parser Content
```Java
{
Name = symantec-edr-json-process-create-success-8001
  ParserVersion = v1.0.0
  Conditions = [  """"product_name":"Symantec Endpoint""", """"event_data_type":"fdr"""",""""type_id":8001""" ]
  Fields = ${SymantecParserTemplates.symantec-parser-template.Fields}[
    """"process":\{.+?"path":"({process_path}({process_dir}(?:[^";]+)?[\\\/;])?({process_name}[^\\\/";]+?))"""",
    """"process":\{.+?cmd_line":"\s*({process_command_line}.+?)\s*",""",
    """"process":\{.+?"pid":({process_id}\d+)""",
    """"actor":\{.+?"path":"({parent_process_path}({parent_process_dir}(?:[^";]+)?[\\\/;])?({parent_process_name}[^\\\/";]+?))""""
  ]

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
      """"user_name":"({user}[\w\.\-]{1,40}\$?)"""",
      """"rule_description":"({additional_info}[^"]+?)\s*"""",
    
}
```