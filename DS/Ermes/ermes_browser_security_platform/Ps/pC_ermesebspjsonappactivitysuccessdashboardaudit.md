#### Parser Content
```Java
{
Name = ermes-ebsp-json-app-activity-success-dashboardaudit
  Conditions = [ """"event_cat":""", """"dashboard_audit"""", """"event_id":""", """"op":""" ]
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
    ]
  }
}
```