#### Parser Content
```Java
{
Name = knowbe4-sat-json-app-activity-success-kmsat
  Vendor = KnowBe4
  Product = Security Awareness Training
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"objectCategory":""", """"activity":"KMSAT_""", """"accountId":""" ]
  Fields = [
    """exa_json_path=$.id,exa_field_name=event_id""",
    """exa_json_path=$.data.objectCategory,exa_field_name=category""",
    """exa_json_path=$.data.objectType,exa_field_name=object_type""",
    """exa_json_path=$.metadata.accountId,exa_field_name=account_id""",
    """exa_json_path=$.metadata.activity,exa_field_name=operation""",
    """exa_json_path=$.metadata.timestamp,exa_field_name=time""",
    """exa_json_path=$.metadata.environment,exa_field_name=region""",
    """exa_json_path=$.schemaVersion,exa_field_name=schema_version"""
  ]
  ParserVersion = "v1.0.0"  


}
```