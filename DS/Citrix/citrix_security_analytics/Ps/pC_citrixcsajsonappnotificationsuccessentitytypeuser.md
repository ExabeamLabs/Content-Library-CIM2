#### Parser Content
```Java
{
Name = citrix-csa-json-app-notification-success-entitytypeuser
  Vendor = Citrix
  Product = Citrix Security Analytics
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"entity_id":"""", """"entity_type":"user"""", """"event_type":"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",   
    """exa_json_path=$.tenant_id,exa_field_name=tenant_id""",
    """exa_json_path=$.entity_id,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.entity_type,exa_field_name=entity_type""",
    """exa_json_path=$.event_type,exa_field_name=event_name""",
    """exa_json_path=$.device,exa_regex=({src_host}[\w.-]+)""",
    """exa_json_path=$.cnt,exa_field_name=count""",
    """exa_json_path=$.city,exa_field_name=city""",
    """exa_json_path=$.country,exa_field_name=country""",
    """exa_json_path=$.cur_riskscore,exa_field_name=risk_score""",
    """exa_json_path=$.client_ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",      
    """exa_json_path=$.session_user_name,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.session_key,exa_field_name=session_id""",
    """exa_json_path=$.device_id,exa_regex=({src_host}[\w.-]+)""",
    """exa_json_path=$.domain,exa_field_name=domain""",
    """exa_json_path=$.server_name,exa_regex=({dest_host}[\w.-]+)""",
    """exa_json_path=$.os_name,exa_field_name=os""",
    """exa_json_path=$.indicator_uuid,exa_field_name=alert_id""",
    """exa_json_path=$.indicator_id,exa_field_name=threat_id""",
    """exa_json_path=$.indicator_category_id,exa_field_name=category_id"""
    """exa_json_path=$.event_id,exa_field_name=event_id""",
    """exa_json_path=$.occurrence_event_type,exa_field_name=event_name""",
  ]
  ParserVersion = "v1.0.0"


}
```