#### Parser Content
```Java
{
Name = checkpoint-avanan-json-alert-trigger-success-severity-1
  Conditions = [ """"sourcetype_s":"avanan_security_event"""", """"event_security_event_entity_info_entity_type_s":"security_event"""" ]
  ParserVersion = v1.0.0

json-avanan-security-alert-1 = {
  Vendor = Check Point
  Product = Check Point Avanan
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Fields = [
    """exa_json_path=$.event_security_event_time_t,exa_field_name=time""",
    """exa_json_path=$.sourcetype_s,exa_field_name=alert_name""",
    """exa_json_path=$.event_security_event_entity_payload_severity_d,exa_field_name=alert_severity""",
    """exa_json_path=$.event_security_event_entity_info_entity_id_g,exa_field_name=alert_id""",
    """exa_json_path=$.event_security_event_entity_info_entity_sub_type_s,exa_field_name=alert_type""",
    """exa_json_path=$.event_entity_entity_payload_subject_s,exa_field_name=email_subject""",
    """exa_json_path=$.event_entity_saas_info_saas_actor_payload_full_name_s,exa_field_name=full_name""",
    """exa_json_path=$.event_entity_saas_info_saas_actor_payload_email_s,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
    """exa_json_path=$.event_entity_entity_payload_from_email_s,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
    """exa_json_path=$.event_entity_entity_payload_recipients_s,exa_regex=^\[\\*"*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\\*"\]$""",
    """exa_json_path=$.event_security_event_entity_payload_description_text_s,exa_field_name=additional_info""",
    """exa_json_path=$.event_entity_entity_payload_is_quarantined_b,exa_field_name=result""",
    """exa_json_path=$.event_entity_entity_payload_sender_client_ip_s,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))$""",
    """exa_json_path=$.event_entity_entity_payload_attachments_s,exa_regex="name\\*":\\*"({email_attachments}[^"\\]+)""",
    """exa_json_path=$.event_security_event_entity_payload_category_s,exa_field_name=category"""
    
}
```