#### Parser Content
```Java
{
Name = exabeam-audit-json-alert-case-success
    Vendor = Exabeam
    Product = Audit Log
    ParserVersion = v1.0.0
    TimeFormat = "epoch"
    ExtractionType = json
    Conditions = [""""activity_type":""", """"application":""", """"subject":""", """"outcome":""", """"operation":"""]
    Fields = [
      """"application":"({app}[^"]+)"""",
      """"subject":"({additional_info}.+?)","""",
      """"object_name":"({object_name}.+?)",""",
      """"object_name":"({rule}.+?)",""",
      """"object_id":"({object_id}[^"]+)"""",
      """"activity_type":"({operation_type}[^"]+)"""",
      """"operation":"({operation}.+?)",""",
      """"operation":"({alert_name}.+?)",""",
      """"old_value":"({old_value}.*?)","""",
      """"new_value":"({new_value}.*?)","""",
      """"old_value":"({old_value}\[.*?\])","\w+":""",
      """"new_value":"({new_value}\[.*?\])","\w+":""",
      """"outcome":"({result}[^"]+)"""",
      """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """"api_method":"({method}[^"]+)"""",
      """"api_endpoint":"({url}[^"]+)"""",
      """"user":"({email_address}[^\@]+@[^"]+)"""",
      """"time":"({time}\d{13})""""
      """"user":"({dest_user}[\w\.\-]+)"""
      """"user":"({user_info}[^"]+)"""
      """exa_json_path=$..application,exa_field_name=app"""
      """exa_json_path=$..subject,exa_field_name=additional_info"""
      """exa_json_path=$..object_name,exa_field_name=object_name"""
      """exa_json_path=$..object_name,exa_field_name=rule"""
      """exa_json_path=$..activity_type,exa_field_name=operation_type"""
      """exa_json_path=$..object_id,exa_field_name=object_id"""
      """exa_json_path=$..operation,exa_field_name=operation"""
      """exa_json_path=$..operation,exa_field_name=alert_name"""
      """exa_json_path=$..old_value,exa_field_name=old_value,exa_match_expr=!InList($..old_value,"")""",
      """exa_json_path=$..new_value,exa_field_name=new_value,exa_match_expr=!InList($..new_value,"")""",
      """exa_json_path=$.old_value,exa_field_name=old_value,exa_match_expr=!InList($.old_value,"")""",
      """exa_json_path=$.new_value,exa_field_name=new_value,exa_match_expr=!InList($.new_value,"")""",
      """exa_json_path=$..outcome,exa_field_name=result"""
      """exa_json_path=$..src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """exa_json_path=$..api_method,exa_field_name=method,exa_match_expr=!InList($..api_method,"")""",
      """exa_json_path=$..api_endpoint,exa_field_name=url,exa_match_expr=!InList($..api_endpoint,"")""",
      """exa_json_path=$.api_endpoint,exa_field_name=url,exa_match_expr=!InList($.api_endpoint,"")""",
      """exa_json_path=$..user,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """exa_json_path=$..time,exa_field_name=time"""
      """exa_json_path=$..user,exa_regex=({dest_user}[\w\.\-]+)"""
      """exa_json_path=$..user,exa_regex=({user_info}[^"]+)"""

    ]
    DupFields = [ "object_name->object" ]
  

}
```