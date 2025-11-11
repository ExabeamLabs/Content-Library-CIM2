#### Parser Content
```Java
{
Name = servicenow-s-json-http-session-success-transcation
  ParserVersion = v1.0.0
  Vendor = ServiceNow
  Product = ServiceNow
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"business_rule_count":""", """"type":""", """"sys_created_on":""", """"sys_created_by":""", """transaction_pattern":""" ]
  Fields = [
    """exa_json_path=$.sys_created_on,exa_field_name=time"""
    """exa_json_path=$.sys_created_by,exa_field_name=user"""
    """exa_json_path=$.protocol,exa_field_name=protocol"""
    """exa_json_path=$.remote_ip,exa_field_name=src_ip""" 
    """exa_json_path=$.link,exa_field_name=url"""
    """exa_json_path=$.user_agent,exa_field_name=user_agent"""
    """exa_json_path=$.output_length,exa_field_name=bytes"""
    """exa_regex=\&sys_original.incident.description=?({additional_info}[^&\r\n]+?)\s*\&"""
    """exa_regex=\&sys_original.incident.number=?({alert_id}[^&]+?)\s*\&"""
    """exa_regex=\&sys_original.incident.category=?({category}[^&]+?)\s*\&"""
    """exa_regex=\&sys_display.incident.assigned_to=?({dest_user}[^&]+?)\s*\&"""
    """exa_regex=\&sys_display.incident.short_description=?({event_name}[^&]+?)\s*\&"""
    """exa_regex=\&sys_display.original.incident.assignment_group=?({group_name}[^&]+?)\s*\&"""
    """exa_regex=\&sys_original.incident.priority=?({priority}[^&]+?)\s*\&"""
    """exa_regex=\&sys_original.incident.subcategory=?({sub_category}[^&]+?)\s*\&"""
    """exa_regex=\&sys_original.incident.state=?({status_msg}[^&]+?)\s*\&"""
    """exa_regex=\&incident.work_notes=?({activity_details}[^&]+?)\s*\&""",
    """exa_regex=\&sys_original.incident.sys_updated_by=?({operator_name}[^&]+?)\s*\&"""
    """exa_regex=\&sys_original.sc_task.number=?({task_id}[^&]+?)\s*\&"""
    """exa_regex=\&sys_display.sc_task.request_item=?({item_name}[^&]+?)\s*\&"""
    """exa_regex=\&sys_original.sc_req_item.number=?({item_name}[^&]+?)\s*\&"""
    """exa_regex=\&sys_original.sc_task.short_description=?({event_name}[^&]+?)\s*\&"""
    """exa_regex=\&sys_display.original.sc_task.assigned_to=?({dest_user}[^&]+?)\s*\&"""
    """exa_regex=\&sys_display.original.sc_task.assignment_group=?({group_name}[^&]+?)\s*\&"""
    """exa_regex=\&sc_task.comments=?({activity_details}[^&\r\n]+?)\s*\&"""
    """exa_regex=\&sys_original.sc_task.description=?({additional_info}[^&\r\n]+?)\s*\&"""
  ]
  DupFields = ["time->incident_creation_time", "event_name->operation"]


}
```