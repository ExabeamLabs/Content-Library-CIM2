#### Parser Content
```Java
{
Name = extremenetworks-uztna-json-app-authentication-applicationaccessinitiated
  Conditions = [""""event":"Application Access Initiated"""", """"event_type":"""", """"event_status":"""", """"performed_by":"""" ]
  ParserVersion = "v1.0.0"

json-extremenetworks-uztna-event = {
  Vendor = Extreme Networks
  Product = Universal ZTNA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.performed_by,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.origin,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
    """exa_json_path=$.event_type,exa_field_name=event_category""",
    """exa_json_path=$.event_status,exa_field_name=result""",
    """exa_json_path=$.event,exa_field_name=event_name""",
    """exa_json_path=$.service_name,exa_field_name=service_name""",
    """exa_json_path=$.service_protocol,exa_field_name=protocol""",
    """exa_json_path=$.service_id,exa_field_name=service_id""",
    """exa_json_path=$.origin_app,exa_field_name=app""",
    """exa_json_path=$.service_name,exa_field_name=app""",    
    """exa_json_path=$.device,exa_field_name=device_name""",
    """exa_json_path=$.os_family,exa_field_name=os""",
    """exa_json_path=$.browser_family,exa_field_name=browser"""    
  
}
```