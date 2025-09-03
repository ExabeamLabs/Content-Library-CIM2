#### Parser Content
```Java
{
Name = swimlane-swimturbine-json-app-activity-catchall
  Vendor = "Swimlane"
  Product = "Swimlane Turbine"
  ExtractionType = "json"
  TimeFormat =[ "yyyy-MM-dd'T'HH:mm:ss" ]
  Conditions = [ """"category":"""", """"eventTime":""", """"actionType":""", """"eventOutcome":"""", """"accountId":"""" ]
  Fields = [
    """exa_json_path=$.sourceIp,exa_regex=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.eventTime,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.userId,exa_field_name=user_id"""
    """exa_json_path=$.category,exa_field_name=category"""
    """exa_json_path=$.actionType,exa_field_name=action"""
    """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
    """exa_json_path=$.accountId,exa_field_name=account_id"""
    """exa_json_path=$.eventOutcome,exa_field_name=result"""
    """exa_json_path=$.userAgent,exa_field_name=user_agent"""
    """exa_json_path=$.authenticationType,exa_field_name=auth_type"""
    """exa_json_path=$.description,exa_field_name=additional_info"""
    """exa_regex=created a user with userName: ({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
  ParserVersion = "v1.0.0"


}
```