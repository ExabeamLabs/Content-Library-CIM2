#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-peripheral_device-enable-connected-5126-1"
  ParserVersion = "v1.0.0"
  Conditions = [ """"dataSource.vendor":"SentinelOne"""", """"activity_type":5126,""", """event_type":"connected"""", """device_name":""", """primary_description":"""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-activity_type.Fields} [
       """exa_json_path=$.['data.device_name'],exa_field_name=device_name""",
       """exa_json_path=$.['data.event_type'],exa_field_name=operation""",
       """exa_json_path=$.['data.last_logged_in_user_name'],exa_field_name=user""",
       """exa_json_path=$.['data.device_class'],exa_field_name=device_class""",
       """exa_json_path=$.['data.interface'],exa_field_name=interface""",
       """exa_json_path=$.['data.event_id'],exa_field_name=event_id"""
  ]

json-sentinelone-activity_type = {
  Vendor = SentinelOne
  Product = "Singularity Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Fields = [
      """exa_json_path=$.timestamp,exa_field_name=time""",
      """exa_json_path=$.site_name,exa_field_name=site_name""",
      """exa_json_path=$.type,exa_field_name=event_name""",  
      """exa_json_path=$.activity_type,exa_field_name=event_code""",    
      """exa_json_path=$.['account.name'],exa_field_name=account_name""",
      """exa_json_path=$.serverIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """exa_json_path=$.group_name,exa_field_name=group_name""" 
      """exa_json_path=$.primary_description,exa_field_name=additional_info"""      
      """exa_json_path=$.['data.ip_address'],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.['data.computer_name'],exa_regex=^({host}[\w.-]+)$""",
      """exa_json_path=$.['device.ip_external'],exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """exa_json_path=$.agent_id,exa_field_name=agent_id""",
      """exa_json_path=$.activity_id,exa_field_name=activity_id""",
  
}
```