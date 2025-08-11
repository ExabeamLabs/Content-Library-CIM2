#### Parser Content
```Java
{
Name = "pingidentity-forgerock-json-endpoint-logout-amlogout"
  Vendor = "Ping Identity"
  Product = "ForgeRock"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  ExtractionType = json
  Conditions = [ """"eventName":"AM-""", """-LOGOUT""", """"component":"Authentication"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.eventName,exa_field_name=event_name"""   
    """exa_json_path=$.transactionId,exa_field_name=message_id"""
    """exa_json_path=$.entries[0].info.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.realm,exa_field_name=realm"""
    """exa_json_path=$.component,exa_field_name=category"""
    """exa_json_path=$.principal[0],exa_field_name=additional_info"""    
    """exa_json_path=$.entries[0].info,exa_field_name=description"""    
    """exa_json_path=$.userId,exa_field_name=user_id"""
    """exa_json_path=$.userId,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,o=({group_name}[^,]+),ou=services,dc=({domain}[^,]+),"""    
  ]
  ParserVersion = "v1.0.0"


}
```