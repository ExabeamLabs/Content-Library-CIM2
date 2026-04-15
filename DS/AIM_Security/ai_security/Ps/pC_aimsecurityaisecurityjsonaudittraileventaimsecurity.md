#### Parser Content
```Java
{
Name = aimsecurity-aisecurity-json-audit-trail-event-aimsecurity
  Vendor = AIM Security
  Product = AI Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [ """"payload_type":"audit_trail_event"""", """"event_id":"""", """"action":"""", """"identity_type":"""" ]
  Fields = [
    """exa_json_path=$.event_timestamp,exa_field_name=time"""
    """exa_json_path=$.event_id,exa_field_name=event_id"""
    """exa_json_path=$.payload_type,exa_field_name=event_name"""
    """exa_json_path=$.action,exa_field_name=action"""
    """exa_json_path=$.user_email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.extra_data.chat_user,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.extra_data.session_id,exa_field_name=session_id"""
    """exa_json_path=$.extra_data.chat_application,exa_field_name=app"""
    """exa_json_path=$.extra_data.new.enabled,exa_field_name=new_value"""
    """exa_json_path=$.extra_data.previous.enabled,exa_field_name=old_value"""
    """exa_json_path=$.extra_data.rule_name,exa_field_name=rule"""
    """exa_json_path=$.extra_data.policy_name,exa_field_name=policy_name"""
    """exa_json_path=$.extra_data.rule_id,exa_field_name=rule_id"""
    """exa_json_path=$.extra_data.report_name,exa_field_name=document_name"""
    """exa_json_path=$.extra_data.report_email_recipients[0],exa_field_name=email_recipients"""
    """exa_json_path=$.extra_data.new.action,exa_field_name=new_value"""
    """exa_json_path=$.extra_data.previous.action,exa_field_name=old_value"""

  ]
  ParserVersion = "v1.0.0"


}
```