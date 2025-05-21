#### Parser Content
```Java
{
Name = 1password-1pwd-json-endpoint-authentication-fail-password_secret_bad
  ParserVersion = v1.0.0
  Vendor = 1password
  Product = 1password
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """uuid""", """"type":"password_secret_bad"""", """"category":"credentials_failed"""", """"client"""" ]
  Fields = [
    """exa_json_path=$.target_user.uuid,exa_field_name=user_uid"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.session_uuid,exa_field_name=session_id"""
    """exa_json_path=$.client.ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.client.app_name,exa_field_name=app"""
    """exa_json_path=$.client.os_name,exa_field_name=os"""
    """exa_json_path=$.target_user.email,exa_field_name=email_address"""
    """exa_json_path=$.type,exa_field_name=operation"""
    """exa_json_path=$.category,exa_field_name=result"""
    """exa_json_path=$.country,exa_field_name=country"""
    """exa_json_path=$.target_user.name,exa_field_name=full_name"""
  ]


}
```