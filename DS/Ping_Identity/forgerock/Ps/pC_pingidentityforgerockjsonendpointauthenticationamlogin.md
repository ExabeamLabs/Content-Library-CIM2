#### Parser Content
```Java
{
Name = "pingidentity-forgerock-json-endpoint-authentication-amlogin"
  Vendor = "Ping Identity"
  Product = "ForgeRock"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  ExtractionType = json
  Conditions = [ """"eventName":"AM-""", """-LOGIN-""", """"component":"Authentication"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.eventName,exa_field_name=event_name"""   
    """exa_json_path=$.transactionId,exa_field_name=message_id"""
    """exa_json_path=$.entries[0].info.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.entries[0].info.authLevel,exa_field_name=auth_level"""
    """exa_json_path=$.realm,exa_field_name=realm"""
    """exa_json_path=$.component,exa_field_name=category"""
    """exa_json_path=$.principal[0],exa_field_name=additional_info"""    
    """exa_json_path=$.entries[0].info,exa_field_name=description"""    
    """exa_json_path=$.userId,exa_field_name=user_id"""
    """exa_json_path=$.userId,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,o=({group_name}[^,]+),ou=services,dc=({domain}[^,]+),"""    
  ]
  ParserVersion = "v1.0.0"
}, 

{
  Name = "pingidentity-forgerock-csv-endpoint-authentication-success-amlogin"
  Vendor = "Ping Identity"
  Product = "ForgeRock"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """FrockAuth""","""AM-""", """-LOGIN-""", """Authentication""" ]
  Fields = [
    """"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)","({event_name}[^",]+)","({message_id}[^",]+)","({user_id}[^"]+)","\["({tracking_id}[^"]+)"\]","({result}[^"]+)","\["({principal_name}[^"]+)"\]"""
    """info":[^\]]+?"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """info":[^\]]+?"authLevel":"({auth_level}[^",]+)""""
    """({category}Authentication)"""  
  ]
  ParserVersion = "v1.0.0"
}, 

{
  Name = "pingidentity-forgerock-str-endpoint-authentication-success-amlogin"
  Vendor = "Ping Identity"
  Product = "ForgeRock"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss"]
  Conditions = [ """Login Success""", """Authentication""", """FrockAuth""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"\s"({event_name}[^"\|]+)"""
    """"\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"({user_id}[^"]+)"\s"""
    """DataStore\s({tracking_id}[^"\s]+)"""
    """({result}Success)"""
    """({category}Authentication)"""  
  ]
  ParserVersion = "v1.0.0"


}
```