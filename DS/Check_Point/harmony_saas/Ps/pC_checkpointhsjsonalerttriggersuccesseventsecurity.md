#### Parser Content
```Java
{
Name = "checkpoint-hs-json-alert-trigger-success-event-security"
 Vendor = Check Point
 Product = Harmony SaaS
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
 ExtractionType = "json"
 ParserVersion = v1.0.0
 Conditions = [ """"event":""", """"security_event":""", """"entity":""", """"saas_info":""", """"confidence_level":""" ]
 Fields  = [
   """exa_json_path=$.event.security_event.entity_info.entity_sub_type,exa_field_name=alert_name"""
   """exa_json_path=$.event.security_event.time,exa_field_name=time"""
   """exa_json_path=$.event.entity.entity_info.customer_farm,exa_field_name=host"""
   """exa_json_path=$.event.security_event.entity_payload.event_metadata.sender_address,exa_field_name=email_address"""
   """exa_json_path=$.event.security_event.entity_payload.description_text,exa_field_name=additional_info"""
   """exa_json_path=$.event.security_event.entity_payload.confidence_level,exa_field_name=alert_severity"""
   """exa_json_path=$.event.security_event.entity_payload.event_trigger.id,exa_field_name=alert_id"""
   """exa_json_path=$.event.security_event.entity_payload.current_state,exa_field_name=alert_status"""
   """exa_json_path=$.event.security_event.saas_info.saas_actor_payload.full_name,exa_field_name=full_name"""
   """exa_json_path=$.event.security_event.saas_info.saas_actor_payload.title,exa_field_name=employee_title"""
   """exa_json_path=$.event.security_event.saas_info.saas_actor_payload.department,exa_field_name=department"""
   """exa_json_path=$.event.security_event.saas_info.saas_actor_payload.email,exa_field_name=email_address"""
   """exa_json_path=$.event.entity.entity_payload.dmarc_result,exa_field_name=dmarc_result"""
   """exa_json_path=$.event.entity.entity_payload.saas_spam_verdict,exa_field_name=spam_score"""
   """exa_json_path=$.event.entity.entity_payload.subject,exa_field_name=email_subject"""
   """exa_regex=entity_type\\":\s*\\"office365_emails_user\\",\s*\\"label\\":\s*\\"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""
   """exa_json_path=$.event.security_event.entity_payload.category,exa_field_name=alert_type"""
 ]


}
```