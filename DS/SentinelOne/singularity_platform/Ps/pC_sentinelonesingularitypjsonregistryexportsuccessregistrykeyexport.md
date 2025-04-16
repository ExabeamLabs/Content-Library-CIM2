#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-registry-export-success-registrykeyexport"
  ExtractionType = json
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"registry"""", """"event.type":"Registry Key Export"""" ]
  DupFields = ["alert_name->event_name"]
  ParserVersion = "v1.0.0"
} 

{
  Vendor = "SentinelOne"
  Product = "Singularity Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
      """exa_json_path=$.timestamp,exa_field_name=time""",
      """exa_json_path=$.operation,exa_field_name=operation""",
      """exa_json_path=$.category_name,exa_field_name=category""",
      """exa_json_path=$.type_name,exa_field_name=operation_type""",
      """exa_json_path=$.['account.id'],exa_field_name=account_id""",
      """exa_json_path=$.['entity.name'],exa_field_name=object""",
      """exa_json_path=$.asset_subcategory,exa_field_name=object_type""",      
      """exa_json_path=$.severity_,exa_field_name=severity""",
      """exa_json_path=$.['account.name'],exa_field_name=account_name""",
      """exa_json_path=$.status,exa_field_name=result""",
      """exa_json_path=$.['s1_metadata.site_name'],exa_field_name=site_name""",
      """exa_json_path=$.message,exa_field_name=event_name""",
      """exa_json_path=$.traceId,exa_field_name=message_id"""      
  ]
  Name = "sentinelone-singularityp-json-app-activity-success-entitymanagement"
  ExtractionType = json
  Conditions = [ """"dataSource.category":"security"""", """vendor_name":"SentinelOne"""", """"class_name":"Entity Management"""" ]
  ParserVersion = "v1.0.0"


}
```