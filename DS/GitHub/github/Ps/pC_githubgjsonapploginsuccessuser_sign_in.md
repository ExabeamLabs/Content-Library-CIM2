#### Parser Content
```Java
{
Name = "github-g-json-app-login-success-user_sign_in"
    Vendor = "GitHub"
    Product = "GitHub"
    TimeFormat = "yyyy-MM-dd HH:mm:ss Z"
    ExtractionType = json
    Conditions = [ """"action":""", """"management_console.user_sign_in"""", """"_document_id":""" ]
    Fields = [
        """exa_json_path=$.path,exa_field_name=additional_info"""
        """exa_json_path=$.method,exa_field_name=method"""
        """exa_json_path=$.mc_actor,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
        """exa_json_path=$.created_at,exa_field_name=time"""
        """exa_json_path=$.user_agent,exa_field_name=user_agent"""
        """exa_json_path=$.session_id,exa_field_name=session_id"""
        """exa_json_path=$.action,exa_field_name=event_name"""
        """exa_json_path=$.actor_location.country_code,exa_field_name=country_code"""
        """exa_json_path=$.actor_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
        """exa_json_path=$._document_id,exa_field_name=doc_id"""        
    ]
    ParserVersion = "v1.0.0"


}
```