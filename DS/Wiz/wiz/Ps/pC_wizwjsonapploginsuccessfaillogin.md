#### Parser Content
```Java
{
Name = wiz-w-json-app-login-success-fail-login
 ParserVersion = "v1.0.0"
 Conditions = [ """"action":"Login"""", """"actionParameters":""" , """"serviceAccount":""", """"sourceIP":""", """"userPoolType":""", """"userpoolID":""" ]

wiz-w-json-audit-log = {
  Vendor = Wiz
  Product = Wiz
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSZ"]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.sourceIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.userAgent,exa_field_name=user_agent"""
    """exa_json_path=$.status,exa_field_name=result"""
    """exa_json_path=$.action,exa_field_name=event_name"""
    """exa_json_path=$.userID,exa_field_name=user"""
    """exa_json_path=$.actionParameters.error,exa_field_name=failure_reason"""
    """exa_json_path=$.userEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  
}
```