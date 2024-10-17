#### Parser Content
```Java
{
Name = symantec-edr-json-file-write-success-8003
  ParserVersion = v1.0.0
  ExtractionType = json
  Conditions = [  """"product_name":"Symantec Endpoint""", """"event_data_type":"fdr"""",""""type_id":8003""" ]
  Fields = ${SymantecParserTemplates.symantec-parser-template.Fields}[
    """exa_json_path=$.file.path,exa_regex=^({file_path}({file_dir}.*?)({file_name}[^\\\/;"]+?(\.({file_ext}[^\.;\\"]+?))?))$""",
    """exa_json_path=$.actor.file.size,exa_field_name=bytes""",
    """exa_json_path=$.type_id,exa_field_name=event_code"""
  ]

symantec-parser-template = {
    Vendor = Symantec
    Product = Symantec Advanced Threat Protection
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd HH:mm:ss"]
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"device_domain":"({domain}[^"]+)"""",
      """"device_name":"({src_host}[\w\-.]+)"""",
      """"device_os_name":"({os}[^"]+)"""",
      """"ipv4":\[?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"user_name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """"rule_description":"({additional_info}[^"]+?)\s*"""",
      """exa_json_path=$.time,exa_field_name=time"""
      """exa_json_path=$.device_domain,exa_field_name=domain"""
      """exa_json_path=$.device_name,exa_field_name=src_host"""
      """exa_json_path=$..ipv4[0],exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$"""
      """exa_json_path=$.device_os_name,exa_field_name=os"""
      """exa_json_path=$.user_name,exa_field_name=user"""
      """exa_regex="time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
      """exa_json_path=$..rule_description,exa_field_name=additional_info"""
    
}
```