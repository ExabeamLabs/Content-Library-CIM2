#### Parser Content
```Java
{
Name = halcyon-halcyon-json-app-activity-success-action
    Vendor = Halcyon
    Product = Halcyon
    ParserVersion = v1.0.0
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ"]
    Conditions = [ """"id":"""", """"tenant_id":"""", """"kind":""", """"action_type":""", """"timestamp":""" ]
    Fields = [
      """exa_json_path=$.timestamp,exa_field_name=time"""
      """exa_json_path=$.action_type,exa_field_name=action"""
      """exa_json_path=$.tenant_id,exa_field_name=tenant_id"""
      """exa_json_path=$.name,exa_field_name=event_name"""
      """exa_json_path=$.description,exa_field_name=additional_info"""
      """exa_json_path=$.device_name,exa_field_name=device_name"""
    ]


}
```