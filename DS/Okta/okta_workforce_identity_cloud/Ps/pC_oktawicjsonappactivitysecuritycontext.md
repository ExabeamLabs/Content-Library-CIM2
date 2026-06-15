#### Parser Content
```Java
{
Name = "okta-wic-json-app-activity-securitycontext"
  Vendor = "Okta"
  Product = "Okta Workforce Identity Cloud"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"eventType":"""", """"legacyEventType"""", """securityContext""", """"outcome_result"""" ]
  Fields = [
    """exa_json_path=$.published,exa_field_name=time""",
    """exa_json_path=$.eventType,exa_field_name=operation""",
    """exa_json_path=$.legacyEventType,exa_field_name=operation_details""",
    """exa_json_path=$.displayMessage,exa_field_name=event_name""",    
    """exa_json_path=$.uuid,exa_field_name=user_uid""",
    """exa_json_path=$.actor_id,exa_field_name=user_id""",
    """exa_regex="actor_type":"User"\s*[^\]\{\}]+?"actor_displayName":"({full_name}[^"]+)"""",
    """exa_regex="actor_displayName":"({full_name}[^"]+)"\s*[^\]\{\}]+?"actor_type":"User"""",
    """exa_regex="actor_type":"(App)?User"\s*[^\]\{\}]+?"actor_alternateId":"({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """exa_regex="actor_alternateId":"({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"\s*[^\]\{\}]+?"actor_type":"(App)?User"""",
    """exa_regex=["|']target["|']:\s*\[[^\]]+?["|']type["|']:\s*["|']AppGroup["|'][^\]\}]+?["|']displayName["|']:\s*["|']({group_name}[^"']+)["|']""",
    """exa_regex=["|']target["|']:\s*\[[^\]]+?["|']displayName["|']:\s*["|']({group_name}[^"']+)["|'][^\]\}]+?["|']type["|']:\s*["|']AppGroup["|']""",
    """exa_regex=["|']target["|']:\s*\[[^\]]+?["|']alternateId["|']:\s*["|']({member}[^"']+)["|'][^\]\}]+?["|']type["|']:\s*["|']AppUser["|']""",
    """exa_json_path=$.target,exa_regex=["|']type["|']:\s*["|'](App)?User["|']\s*[^\}]+?["|']alternateId["|']:\s*["|']({member}[^"']+)["|']""",
    """exa_json_path=$.target,exa_regex=["|']type["|']:\s*["|'](App)?User["|']\s*[^\}]+?["|']alternateId["|']:\s*["|'](({dest_email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"'\\,;\|]+\.[^\]\s"'\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))["|']""",
    """exa_json_path=$.target,exa_regex=["|']type["|']:\s*["|']AppGroup["|']\s*[^\}]+?["|']displayName["|']:\s*["|']({group_name}[^"']+)["|']""",    """exa_json_path=$.client_ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.client_useragent_rawUserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.client_useragent_browser,exa_field_name=browser""",
    """exa_json_path=$.client_useragent_os,exa_field_name=os""",
    """exa_json_path=$.client_geographicalContext_city,exa_field_name=location_city""",
    """exa_json_path=$.client_geographicalContext_state,exa_field_name=location_state""",
    """exa_json_path=$.client_geographicalContext_country,exa_field_name=location_country""",
    """exa_json_path=$.outcome_result,exa_field_name=result""",
    """exa_json_path=$.outcome_reason,exa_field_name=failure_reason""",
    """exa_json_path=$.securityContext_domain,exa_field_name=domain""",
    """exa_json_path=$.severity,exa_field_name=severity"""
  ]
  ParserVersion = "v1.0.0"


}
```