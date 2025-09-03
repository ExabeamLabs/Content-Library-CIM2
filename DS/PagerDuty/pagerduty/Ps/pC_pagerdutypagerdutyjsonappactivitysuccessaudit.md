#### Parser Content
```Java
{
Name = pagerduty-pagerduty-json-app-activity-success-audit
   Product = PagerDuty
   Vendor = PagerDuty
   TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]
   ParserVersion = v1.0.0
   ExtractionType = json
   Conditions = [  """"id":""", """"execution_time":""", """"action":""" , """"details":""", """"execution_context":""", """"resource":""", """"root_resource":"""]
   Fields  = [
	  """exa_json_path=$.action,exa_field_name=action""",
    """exa_json_path=$.actors[0].type,exa_field_name=object_type""",
    """exa_json_path=$.actors[0].id,exa_field_name=object_id"""
    """exa_json_path=$.details.resource.id,exa_field_name=resource_id""",
    """exa_json_path=$.details.resource.summary,exa_field_name=additional_info""",
    """exa_json_path=$.details.resource.type,exa_field_name=resource_type""",
    """exa_json_path=$.execution_context.request_id,exa_field_name=app_id""",
    """exa_json_path=$.execution_time,exa_field_name=time""",
    """exa_json_path=$.id,exa_field_name=audit_id""",
    """exa_json_path=$.method.type,exa_field_name=service_name""",
    """exa_json_path=$.details.fields[0].before_value,exa_field_name=more_info""",
    """exa_json_path=$.details.fields[0].name,exa_field_name=object_name"""
    ]
   
 

}
```