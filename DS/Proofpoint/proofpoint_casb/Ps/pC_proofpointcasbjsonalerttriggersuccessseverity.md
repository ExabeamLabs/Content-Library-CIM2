#### Parser Content
```Java
{
Name = "proofpoint-casb-json-alert-trigger-success-severity"
  Conditions = [
  """"sub_type": "Suspicious Activity""""
  """"related_events_0_event_id":"""
  """"related_events_0_user_email":"""
  """"severity":"""
  ]
  ParserVersion = "v1.0.0"

proofpoint-casb-json-alert-trigger-events = {
  Vendor = "Proofpoint"
  Product = "Proofpoint CASB"
  TimeFormat = "epoch"
  ExtractionType = json
  Fields = [
      """exa_json_path=$.timestamp,exa_field_name=time""",
      """exa_json_path=$.related_events_0_intelligence_0_ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.title,exa_field_name=alert_name""",
      """exa_json_path=$.severity,exa_field_name=alert_severity""",
      """exa_json_path=$.sub_type,exa_field_name=alert_type""",
      """exa_json_path=$.related_events_0_event_classification_category,exa_field_name=event_name""",
      """exa_json_path=$.related_events_0_full_name,exa_field_name=full_name""",
      """exa_json_path=$.related_events_0_user_email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """exa_json_path=$.id,exa_field_name=alert_id""",
      """exa_json_path=$.description,exa_field_name=additional_info""",
      """exa_json_path=$.related_events_0_cloud_service,exa_field_name=target""",
      """exa_json_path=$.related_events_0_user_agent,exa_field_name=user_agent"""
    
}
```