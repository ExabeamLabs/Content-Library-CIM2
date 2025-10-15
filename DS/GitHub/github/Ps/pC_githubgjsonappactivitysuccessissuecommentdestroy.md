#### Parser Content
```Java
{
Name = github-g-json-app-activity-success-issuecommentdestroy
  ParserVersion = "v1.0.0"
  Conditions = [ """"action":""", """"issue_comment.destroy"""", """"operation_type":""", """"remove"""" ]

json-github-actions-1 = {
    Vendor = GitHub
    Product = GitHub
    TimeFormat = ["epoch","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
	  ExtractionType = json
    Fields = [
      """exa_json_path=$..@timestamp,exa_field_name=time"""
      """exa_json_path=$..action,exa_field_name=operation"""
      """exa_json_path=$..user_agent,exa_field_name=user_agent"""
      """exa_json_path=$..actor_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """exa_json_path=$..repo,exa_field_name=object"""
      """exa_json_path=$..repo,exa_field_name=repository_name"""
      """exa_json_path=$..actor,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
      """exa_json_path=$..user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
      """exa_json_path=$..operation_type,exa_field_name=operation_type"""
      """exa_json_path=$..application_name,exa_field_name=app"""
      """exa_json_path=$..status_code,exa_field_name=status_msg"""
      """exa_json_path=$..key,exa_field_name=key_name"""
      """exa_json_path=$..external_identity_username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """exa_json_path=$..external_identity_nameid,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """exa_json_path=$..external_identity_username,exa_regex=^[^@"]+?@({domain}[^"]+)$""",
      """exa_json_path=$..external_identity_nameid,exa_regex=^[^@"]+?@({domain}[^"]+)$"""
      """exa_json_path=$..service,exa_field_name=service_name"""
      """exa_json_path=$._document_id,exa_field_name=doc_id"""
      """exa_json_path=$.programmatic_access_type,exa_field_name=access_type"""
      """exa_json_path=$.user_agent,exa_field_name=user_agent"""
      """exa_json_path=$.user_id,exa_field_name=user_id"""
      """exa_json_path=$.business,exa_field_name=company"""
      """exa_json_path=$.actor_location.country_code,exa_field_name=country_code"""
      """exa_json_path=$.request_method,exa_field_name=method"""
      """exa_json_path=$.url_path,exa_field_name=uri_path"""
      """exa_json_path=$.query_string,exa_field_name=query"""
    
}
```