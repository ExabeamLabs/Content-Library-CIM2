#### Parser Content
```Java
{
Name = 1password-1pwd-json-endpoint-app-activity-catchall
  Conditions = [ """"date":""", """"service":"1password"""", """"attributes":""", """"tags":""", """"uuid":""" ]
  ParserVersion = "v1.0.0"

1password-app-activity = {
    Vendor = 1password
    Product = 1password
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
       """exa_json_path=$.date,exa_field_name=time"""
       """exa_json_path=$.source,exa_field_name=app"""
       """exa_json_path=$.session_uuid,exa_field_name=session_id"""
       """exa_json_path=$.attributes.evt.name,exa_field_name=action"""
       """exa_json_path=$.attributes.evt.type,exa_field_name=operation"""
       """exa_json_path=$.attributes.usr.name,exa_field_name=full_name"""
       """exa_json_path=$.attributes.usr.email,exa_field_name=email_address"""
       """exa_json_path=$.attributes.object_details.email,exa_field_name=dest_email_address"""
       """exa_json_path=$.attributes.network.client.ip,exa_field_name=src_ip"""
       """exa_json_path=$.attributes.network.client.geoip.country.name,exa_field_name=country"""
       """exa_json_path=$.attributes.network.client.geoip.subdivision.name,exa_field_name=location_state"""
       """exa_json_path=$.attributes.network.client.geoip.city.name,exa_field_name=location_city"""
       """exa_json_path=$.attributes.session.uuid,exa_field_name=session_id"""
       """exa_json_path=$.attributes.object_type,exa_field_name=object_type"""
       """exa_json_path=$.attributes.aux_details.uuid,exa_field_name=user_uid"""
       ]
     }
  }

mimecast-json-template = {
  mimecast-json-event = {
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Fields = [
      """exa_json_path=$.eventTime,exa_field_name=time"""
      """exa_json_path=$.auditType,exa_field_name=operation"""
      """exa_json_path=$.category,exa_field_name=category"""
      """exa_json_path=$.event.action,exa_field_name=action"""
      """exa_json_path=$.event.category[0],exa_field_name=event_category"""
      """exa_json_path=$.event.outcome,exa_field_name=result"""
      """exa_json_path=$.event.reason,exa_field_name=result_reason"""
      """exa_json_path=$.eventInfo,exa_field_name=additional_info"""
      """exa_json_path=$.id,exa_field_name=event_id"""
      """exa_json_path=$.network.application,exa_field_name=app"""
      """exa_json_path=$.source.ip,exa_field_name=src_ip"""
      """exa_json_path=$.user.domain,exa_field_name=domain"""
      """exa_json_path=$.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """exa_json_path=$.user.name,exa_field_name=user"""
      """exa_json_path=$.user.fullname,exa_field_name=full_name"""
      
}
```