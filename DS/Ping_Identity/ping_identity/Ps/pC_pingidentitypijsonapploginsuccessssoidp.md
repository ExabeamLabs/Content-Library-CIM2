#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-login-success-ssoidp
  ParserVersion = "v1.0.0"
  Conditions = [ """"action":{"type":"SSO_IDP"}""" ]

json-ping-events = {
  Vendor = Ping Identity
  Product = Ping Identity
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-dd-MM'T'HH:mm:ss.SSSZ"
  Fields = [
    """exa_json_path=$.recorded,exa_field_name=time"""
    """exa_json_path=$.client.id,exa_field_name=user_agent"""
    """exa_json_path=$.resources[2].name,exa_field_name=app"""
    """exa_json_path=$.result.status,exa_field_name=result"""
    """exa_json_path=$.result.message,exa_field_name=result_reason"""
    """exa_json_path=$.source,exa_field_name=alert_source"""
    """exa_json_path=$.action.type,exa_field_name=event_name"""
    """exa_json_path=$.resources.subject,exa_field_name=operation"""	
    """exa_regex="ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex="actors":[^"]+"name":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  
}
```