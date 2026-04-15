#### Parser Content
```Java
{
Name = ermes-ebsp-json-alert-trigger-success-datalossprevention
  Conditions = [ """"event_cat":""", """"data_loss_prevention"""", """"event_id":""", """"op":""" ]
  Fields = ${ErmesParsersTemplates.json-ermes-app-activity.Fields}[
    """exa_json_path=$..dlp_details.device_name,exa_field_name=device_name"""
    """exa_json_path=$..dlp_details.agent_id,exa_field_name=agent_id"""
    """exa_json_path=$..dlp_details.file_type,exa_field_name=file_type"""
    """exa_json_path=$..dlp_details.host,exa_field_name=host"""
    """exa_json_path=$..dlp_details.policy_name,exa_field_name=policy_name"""
    """exa_json_path=$..dlp_details.user_agent,exa_field_name=user_agent"""
    """exa_json_path=$..dlp_details.timestamp,exa_field_name=time"""
  ]
  ParserVersion = "v1.0.0"

json-ermes-app-activity = {
    Vendor = "Ermes"
    Product = "Ermes Browser Security Platform"
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [
      """exa_json_path=$.event_cat,exa_field_name=event_category"""
      """exa_json_path=$.event_id,exa_field_name=event_name"""
      """exa_json_path=$.level,exa_field_name=severity"""
      """exa_json_path=$._created,exa_field_name=time"""
      """exa_json_path=$.client_ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$"""
      """exa_json_path=$..op,exa_field_name=operation"""
      """exa_json_path=$..resource,exa_field_name=resource"""
      """exa_json_path=$.message.en,exa_field_name=additional_info"""
      """exa_json_path=$.username,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?))$"""
    
}
```