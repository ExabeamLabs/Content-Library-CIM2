#### Parser Content
```Java
{
Name = onewelcome-ocip-json-app-authentication-fail-430102
  Conditions = [ """"originator":"onewelcome"""", """"siemcode":"430102"""", """"result":"FAIL"""", """"logtype":"AUDIT"""" ]
  ParserVersion = "v1.0.0"

onewelcome-authentication-event = {
    Vendor = OneWelcome
    Product = OneWelcome Cloud Identity Platform
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """exa_json_path=$.['@timestamp'],exa_field_name=time""",
      """exa_json_path=$.account,exa_regex=(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)""",
      """exa_json_path=$.clientip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.siemcode,exa_field_name=event_code""",
      """exa_json_path=$.useragent,exa_field_name=user_agent""",
      """exa_json_path=$.app,exa_regex=\/?({app}[^"]+)""",
      """exa_json_path=$.type,exa_field_name=auth_type""",
      """exa_json_path=$.pepmod,exa_field_name=object""",
      """exa_json_path=$.result,exa_field_name=result""",
      """exa_json_path=$.authres,exa_field_name=result""",
      """exa_json_path=$.action,exa_field_name=event_name""",
      """exa_json_path=$.action,exa_field_name=operation""",
      """exa_json_path=$.hdetail,exa_field_name=additional_info""",
      """exa_json_path=$.human,exa_field_name=additional_info"""
    
}
```