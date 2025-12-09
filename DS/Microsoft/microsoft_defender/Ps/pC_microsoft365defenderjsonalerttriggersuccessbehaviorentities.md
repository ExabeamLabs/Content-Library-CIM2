#### Parser Content
```Java
{
Name = "microsoft-365defender-json-alert-trigger-success-behaviorentities"
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"category":"AdvancedHunting-BehaviorEntities"""", """"operationName":"Publish"""", """"BehaviorId":"""" ]
  Fields = [
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"tenantId":"({tenant_id}[^"]+)"""",
    """"(C|c)ategory":"({alert_type}[^"]+)"""",
    """"ActionType":"({event_name}[^"]+)""",
    """"RemoteIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"FileName":"({file_name}[^"]+)""",
    """"FolderPath":"({file_path}[^"]+)""",
    """"EntityType":"({entity_type}[^"]+)""",
    """"AccountSid":"({user_sid}[^"]+)""",
    """"DeviceName":"({src_host}[^"]+)""",
    """"AccountName":"(null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"Categories":"\[({categories}[^\]]+)"""",
    """"ServiceSource":"({service_name}[^"]+)"""",
    """"DetectionSource":"({alert_source}[^"]+)"""",
    """"AccountDomain":"({domain}[^"]+)"""",
    """"AccountUpn":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"LocalIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$..tenantId,exa_field_name=tenant_id""",
    """exa_json_path=$..category,exa_field_name=alert_type""",
    """exa_json_path=$..Category,exa_field_name=alert_type""",
    """exa_json_path=$..ActionType,exa_field_name=event_name""",
    """exa_json_path=$..FileName,exa_field_name=file_name""",
    """exa_json_path=$..FolderPath,exa_field_name=file_path""",
    """exa_json_path=$..EntityType,exa_field_name=entity_type""",
    """exa_json_path=$..AccountSid,exa_field_name=user_sid""",
    """exa_json_path=$..DeviceName,exa_field_name=src_host""",
    """exa_json_path=$..Categories,exa_field_name=categories""",
    """exa_json_path=$..ServiceSource,exa_field_name=service_name""",
    """exa_json_path=$..DetectionSource,exa_field_name=alert_source""",
    """exa_json_path=$..AccountDomain,exa_field_name=domain""",
    """exa_json_path=$..RemoteIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$..LocalIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$..AccountUpn,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),exa_match_expr=!Contains(tolower($..AccountUpn), "null")""",
    """exa_json_path=$..AccountName,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?),exa_match_expr=!Contains(tolower($..AccountName), "null")"""
]
  ParserVersion = "v1.0.0"


}
```