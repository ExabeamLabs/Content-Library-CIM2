#### Parser Content
```Java
{
Name = "zeronetworks-zeronetworks-json-app-activity-success-auditlogevent"
  Vendor = "Zero Networks"
  Product = "Zero Networks"
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ """"auditType":""" ,""""enforcementSource":""" , """"id":"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.parentObjectId,exa_field_name=object_id"""
    """exa_json_path=$.details,exa_regex=localEntityNames\\?":\{\\?"id\\?":\\?"({source_device_entity_id}[^"\\]+)\\?""""
    """exa_json_path=$.details,exa_regex=remoteEntityNames\\?":\[\{\\?"id\\?":\\?"({dest_device_entity_id}[^"\\]+)\\?""""
    """exa_json_path=$.destinationEntitiesList,exa_field_name=entities"""
    """exa_json_path=$.auditType,exa_field_name=audit_id"""
    """exa_json_path=$.userRole,exa_field_name=role_id"""
    """exa_json_path=$.enforcementSource,exa_field_name=result_code"""
    """exa_json_path=$.details,exa_regex=description\\?":\\?"({description}[^\\"]+)\\?","""
  ]
  DupFields = [ "operation->access" ]
  ParserVersion = "v1.0.0"


}
```