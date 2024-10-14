#### Parser Content
```Java
{
Name = salesforce-sf-json-app-activity-success-type
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """destinationServiceName =Sales Cloud""", """"type":""", """"Id":""", """"attributes":""" ]
  Fields = [
    """exa_regex=({app}Sales Cloud)"""
    """exa_json_path=$.CreatedDate,exa_regex=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.CreatedBy.Email,exa_field_name=email_address""",
    """exa_json_path=$.CreatedBy.Username,exa_regex=(autoproc|({user}[\w\.\-]{1,40}\$?))(@({domain}[^"@]+))?""",
    """exa_json_path=$.CreatedBy.Id,exa_field_name=user_id""",
    """exa_json_path=$.CreatedBy.Name,exa_regex=((Automated Process)|({full_name}[^"]+))""",
    """exa_json_path=$.attributes.url,exa_field_name=object"""
    """exa_json_path=$.attributes.type,exa_field_name=event_category"""
    """exa_json_path=$.Id,exa_field_name=object_id"""
    """exa_json_path=$.Name,exa_field_name=object_name"""
  ]


}
```