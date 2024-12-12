#### Parser Content
```Java
{
Name = servicenow-s-json-app-activity-success-syscreated
  Vendor = ServiceNow
  Product = ServiceNow
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions= [ """"sys_created_on":""", """"sys_created_by":""", """"work_notes":""", """"display_value":""", """"upon_reject":""" ]
  Fields =[
  	"""exa_json_path=$.sys_created_on.value,exa_field_name=time""",
  	"""exa_json_path=$.description.value,exa_field_name=additional_info""",
  	"""exa_json_path=$.short_description.value,exa_field_name=event_name""",
  	"""exa_json_path=$.category.value,exa_field_name=category""",
  	"""exa_json_path=$.priority.display_value,exa_field_name=priority""",
  	"""exa_json_path=$.short_description.value,exa_field_name=operation""",
  	"""exa_json_path=$.cat_item.display_value,exa_field_name=operation""",
  	"""exa_json_path=$.state.display_value,exa_field_name=state"""
  	"""exa_json_path=$.number.display_value,exa_field_name=alert_id"""
  	"""exa_json_path=$.assignment_group.display_value,exa_field_name=group_name"""
  	"""exa_json_path=$.sys_created_by.display_value,exa_field_name=user"""
  	"""exa_json_path=$.assigned_to.display_value,exa_field_name=dest_user"""
  ]
  DupFields = ["time->incident_creation_time"]


}
```