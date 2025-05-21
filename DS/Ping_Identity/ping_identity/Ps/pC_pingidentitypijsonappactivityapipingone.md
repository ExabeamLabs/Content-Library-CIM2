#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-activity-apipingone
  Conditions = [ """"action":{"type":"""", """api.pingone.com""" ]
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = ${PingParsersTemplates.json-ping-events.Fields}[
    """exa_json_path=$.recordedAt,exa_field_name=time"""
    """exa_json_path=$.actors.client.id,exa_field_name=client_id"""
    """exa_json_path=$.actors.client.name,exa_field_name=client_name"""
    """exa_json_path=$.actors.client.type,exa_field_name=client_type"""
    """exa_json_path=$.action.description,exa_field_name=additional_info"""
    """exa_json_path=$.result.description,exa_field_name=more_info"""
    """exa_json_path=$.source.userAgent,exa_field_name=user_agent"""
    """exa_json_path=$.actors.user.name,exa_field_name=user"""
    """exa_json_path=$.actors.client.name,exa_field_name=client"""
    """exa_json_path=$.resources[?(@.type == 'USER')].name,exa_field_name=user"""
    """exa_json_path=$.resources[?(@.type == 'SESSION')].id,exa_field_name=session_id"""
  ]

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
    """exa_regex="ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex="actors":[^"]+"name":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  
}
```