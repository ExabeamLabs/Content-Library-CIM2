#### Parser Content
```Java
{
Name = github-g-json-key-delete-success-publickeydelete
  ParserVersion = "v1.0.0"
  Conditions = [ """"action":""", """"public_key.delete"""", """"operation_type":""", """"remove"""" ]

json-github-actions-1 = {
    Vendor = GitHub
    Product = GitHub
    TimeFormat = ["epoch","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
	  ExtractionType = json
    Fields = [
      """exa_json_path=$.@timestamp,exa_field_name=time"""
      """exa_json_path=$.action,exa_field_name=operation"""
      """exa_json_path=$.user_agent,exa_field_name=user_agent"""
      """exa_json_path=$.actor_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """exa_json_path=$.repo,exa_field_name=object"""
      """exa_json_path=$.actor,exa_regex=({user}[\w\.\-]{1,40}\$?)"""
      """exa_json_path=$.user,exa_regex=({user}[\w\.\-]{1,40}\$?)"""
      """exa_json_path=$.operation_type,exa_field_name=operation_type"""
      """exa_json_path=$.application_name,exa_field_name=app"""
      """exa_json_path=$.status_code,exa_field_name=status_code"""
      """exa_json_path=$.key,exa_field_name=key_name"""
    
}
```