#### Parser Content
```Java
{
Name = google-geminient-json-ai_agent-request-discoveryengine
  ExtractionType = json
  Vendor = Google
  Product = Gemini Enterprise
  ParserVersion = "v1.0.0"
  TimeFormat = [ """yyyy-MM-dd'T'HH:mm:ss.SSSZ""", """yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ""" ]
  Conditions = [ """"methodName":""", """"serviceName":""", """"google.cloud.discoveryengine.""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$..authenticationInfo.principalEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$..authenticationInfo.principalSubject,exa_regex=[^\\,]+\/({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_regex="resourceName":[^\]\},]+?engines\/({app_id}[^\/,]+?)\/"""
    """exa_json_path=$..response.assistToken,exa_field_name=identifier""",
    """exa_json_path=$..requestMetadata.callerIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d).?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$..serviceName,exa_field_name=service_name"""
  ]


}
```