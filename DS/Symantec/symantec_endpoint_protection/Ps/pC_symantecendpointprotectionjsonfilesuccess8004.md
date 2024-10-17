#### Parser Content
```Java
{
Name = symantec-endpointprotection-json-file-success-8004
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Conditions = [ """"type_id":8004,""",""""product_name":"Symantec Endpoint""" ]
  Fields = ${SymantecParsersTemplates.json-symantec-endpoint-protection.Fields}[
    """exa_json_path=$.id,exa_field_name=operation"""
    """exa_json_path=$.type_id,exa_field_name=event_code"""
    """exa_json_path=$.directory.path,exa_field_name=file_path"""
    """exa_json_path=$.directory.folder,exa_field_name=file_dir"""
	  """exa_regex="rule_name":"({event_name}[^"]+)"""",
	  """exa_regex="rule_description":"({additional_info}[^"]+)"""",
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
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","epoch"]
    Fields = [
      """"time\\*":({time}\d{13})"""
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"message":"\s*({additional_info}[^"]+)""",
      """"user_name":"(({domain}[^\\"]+)\\\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """"uuid":"({user_uid}[^"]+)""",
      """"destinationServiceName":"({app}[^"]+)""",
      """"session_id":"({session_id}[^"]+)""",
      """"device_public_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"device_os_name":"({os}[^"]+)""",
      """"device_name":"({host}[\w\-.]+)""",
      """"device_domain":"({domain}[^"]+)""",
      """"rule_name":"({operation}[^"]+)"""
      """exa_json_path=$.time,exa_field_name=time"""
      """exa_regex="time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """exa_json_path=$.message,exa_field_name=additional_info"""
      """exa_json_path=$.uuid,exa_field_name=user_uid"""
      """exa_json_path=$.session_id,exa_field_name=session_id"""
      """exa_json_path=$.destinationServiceName,exa_field_name=app"""
      """exa_json_path=$.device_public_ip,exa_field_name=src_ip"""
      """exa_json_path=$.device_os_name,exa_field_name=os"""
      """exa_json_path=$.device_name,exa_field_name=host"""
      """exa_json_path=$.device_domain,exa_field_name=domain"""
      """exa_json_path=$..rule_name,exa_field_name=operation"""
      """exa_json_path=$.user_name,exa_regex=^(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$"""
    ]
   DupFields = [ "host->src_host" 
}
```