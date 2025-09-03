#### Parser Content
```Java
{
Name = auth0-a-json-app-login-success-ss
  Conditions = [
    """"type":"ss""""
    """"user_id""""
    """"client_name""""
    """"client_id"""
  ]
  ParserVersion = "v1.0.0"

auth0-authentication-template = {
    Vendor = Auth0
    Product = Auth0
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Fields = [
      """date"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)""",
      """hostname"+:"+({host}[^"]+)""",
      """description"+:"+({additional_info}[^"]+)\s*"+""",
      """"+ip"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """user_id"+:"+((({auth_type}[^|"]+)\|({domain}[^|"]+)\|([\w\.\-]{1,40}\$?))|(({=auth_type}[^|"]+)\|))"""
      """user_id":"([^\|]+\|){2}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
      """user_name"+:"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))"""",
      """client_name"+:"+({app}[^"]+)""",
      """user_agent"+:"+({user_agent}[^"]+)""",         
      """severity"+:"+({alert_severity}[^"]+)""", 
      """"type":"({operation_type}[^",]+)""""
      """exa_json_path=$..date,exa_field_name=time"""
      """exa_json_path=$..hostname,exa_field_name=host"""
      """exa_json_path=$.message.description,exa_field_name=additional_info"""
      """exa_json_path=$..ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$..user_id,exa_regex=((({auth_type}[^|"]+)\|({domain}[^|"]+)\|([\w\.\-]{1,40}\$?))|(({=auth_type}[^|"]+)\|))"""
      """exa_json_path=$..user_id,exa_regex=([^\|]+\|){2}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
      """exa_json_path=$..client_name,exa_field_name=app"""
      """exa_json_path=$..user_agent,exa_field_name=user_agent"""
      """exa_json_path=$..severity,exa_field_name=alert_severity"""
      """exa_json_path=$.message.type,exa_regex=({operation_type}[^",]+)"""
      """exa_json_path=$.data..user.email,exa_field_name=email_address"""
      """exa_json_path=$..user_name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))"""
      """exa_json_path=$.data..request.userAgent,exa_field_name=user_agent"""
      """exa_json_path=$.data..request.path,exa_field_name=uri_path"""
      """exa_json_path=$.data..request.method,exa_field_name=method"""
      """exa_json_path=$.data..response.statusCode,exa_field_name=http_response_code"""
      """exa_json_path=$.data.type,exa_field_name=operation_type"""
      """exa_json_path=$.data.description,exa_field_name=additional_info"""
      """exa_json_path=$..request.ip,exa_field_name=src_ip"""
    
}
```