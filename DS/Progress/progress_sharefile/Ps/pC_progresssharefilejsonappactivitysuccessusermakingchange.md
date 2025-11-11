#### Parser Content
```Java
{
Name = "progress-sharefile-json-app-activity-success-usermakingchange"
  Vendor = "Progress"
  Product = "Progress ShareFile"
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  ExtractionType = json  
  Conditions = [ """destinationServiceName =Progress ShareFile""", """"Action":""", """"ActivityType":""", """"UserMakingChangeEmailAddress":""" ]
  Fields = [
    """exa_json_path=$.Path,exa_field_name=uri_path""",
    """exa_regex="Path":\s*"({file_path}\/*({file_dir}[^"]*?[\/]+)?({file_name}[^\/",]+?(\.({file_ext}[^\/"\.\s,]+))?))"""",
    """exa_json_path=$.AdditionalInfo,exa_field_name=additional_info""",
    """exa_json_path=$.Action,exa_field_name=action""",
    """exa_json_path=$.ActivityType,exa_field_name=operation""",
    """exa_json_path=$.ChangeSourceIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.TimeStamp,exa_field_name=time""",
    """exa_regex="Path":\s*"({src_file_path}\/*({src_file_dir}[^"]*?[\/]+)?({src_file_name}[^\/",]+?(\.({src_file_ext}[^\/"\.\s,]+))?))"""",
    """exa_json_path=$.UserMakingChangeEmailAddress,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.UserMakingChange,exa_field_name=full_name""",
    """exa_json_path=$.ActionDetails,exa_field_name=file_permissions""",  
    """exa_regex=({app}Progress ShareFile)"""      
  ]
  ParserVersion = v1.0.0


}
```