#### Parser Content
```Java
{
Name = symantec-endpointprotection-json-file-success-8004
  ParserVersion = "v1.0.0"
  Conditions = [ """"type_id":8004,""",""""product_name":"Symantec Endpoint Security"""" ]
  Fields = ${SymantecParsersTemplates.json-symantec-endpoint-protection.Fields}[
    """"id":({operation}\d+)""",
	  """"directory".+?path":"({file_path}[^"]+)"""",
	  """"directory".+?folder":"({file_dir}[^"]+)"""",
	  """"rule_name":"({event_name}[^"]+)"""",
	  """"rule_description":"({additional_info}[^"]+)"""",
	  """"type_id":({event_code}8004)"""
  ]

json-symantec-endpoint-protection = {
    Vendor = Symantec
    Product = Symantec Endpoint Protection
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"message":"\s*({additional_info}[^"]+)""",
      """"user_name":"(({domain}[^\\"]+)\\\\)?({user}[\w\.\-]{1,40}\$?)""",
      """"uuid":"({user_uid}[^"]+)""",
      """"destinationServiceName":"({app}[^"]+)""",
      """"session_id":"({session_id}[^"]+)""",
      """"device_public_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"device_os_name":"({os}[^"]+)""",
      """"device_name":"({host}[\w\-.]+)""",
      """"device_domain":"({domain}[^"]+)""",
      """"rule_name":"({operation}[^"]+)"""
    
}
```