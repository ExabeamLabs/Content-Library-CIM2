#### Parser Content
```Java
{
Name = armorblox-ab-json-email-abuse
  Conditions = [ """"incident_type":"ABUSE_INCIDENT_TYPE"""", """"resolution_state":""", """"remediation_actions":""" ]
  ParserVersion = "v1.0.0"

armorblox-email = {
  Vendor = Armorblox
  Product = Armorblox
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Fields = [
    """exa_json_path=$.date,exa_field_name=time""",
    """exa_json_path=$.title,exa_field_name=email_subject""",
    """exa_json_path=$.original_sender_address,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.users[0].email,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.app_name,exa_field_name=app""",
    """exa_json_path=$.remediation_actions[0],exa_field_name=operation""",
    """exa_json_path=$.folder_categories[0],exa_field_name=category""",
    """exa_json_path=$.priority,exa_field_name=priority""",
    """exa_json_path=$.incident_type,exa_field_name=event_name""",
    """exa_json_path=$.attachment_list[0],exa_field_name=email_attachments""",
    """exa_regex="attachment_list":\["({email_attachment}[^,]*(\.({file_ext}[^",\]]+)))"""
   
}
```