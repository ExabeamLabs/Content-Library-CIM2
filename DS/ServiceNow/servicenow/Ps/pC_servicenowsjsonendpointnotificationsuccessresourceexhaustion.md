#### Parser Content
```Java
{
Name = servicenow-s-json-endpoint-notification-success-resourceexhaustion
    ParserVersion = v1.0.0
    Conditions= [ """"sys_created_on":""", """"sys_created_by":""", """"type":"Resource Exhaustion Event Detected"""" ]

servicenow-json-template = {
    Vendor = ServiceNow
    Product = ServiceNow
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields =[
        """exa_json_path=$.sys_created_on,exa_field_name=time""",
        """exa_json_path=$.sys_created_by,exa_field_name=user"""
        """exa_json_path=$.description,exa_field_name=description""",
        """exa_json_path=$.state,exa_field_name=state"""
        """exa_json_path=$.type,exa_field_name=alert_type"""
        """exa_json_path=$.processing_notes,exa_field_name=rule_description"""
        """exa_json_path=$.severity,exa_field_name=severity"""
        """exa_json_path=$.resource,exa_field_name=resource"""
        """exa_json_path=$.node,exa_field_name=host"""
        """exa_json_path=$.additional_info,exa_field_name=additional_info"""
    ]
    DupFields = ["time->incident_creation_time"
}
```