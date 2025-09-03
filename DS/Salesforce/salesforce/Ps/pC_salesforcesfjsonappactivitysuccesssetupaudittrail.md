#### Parser Content
```Java
{
Name = salesforce-sf-json-app-activity-success-setupaudittrail
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"type":"SetupAuditTrail"""", """"Action":"""", """"Display":"""" ]
  Fields = [
    """exa_json_path=$.CreatedDate,exa_regex=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.Action,exa_field_name=operation""",
    """exa_json_path=$.CreatedBy.Email,exa_field_name=email_address""",
    """exa_json_path=$.CreatedBy.Username,exa_regex=(autoproc|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^"@]+))?""",
    """exa_json_path=$.CreatedBy.Id,exa_field_name=user_id""",
    """exa_json_path=$.CreatedBy.Name,exa_regex=((Automated Process)|({full_name}[^"]+))""",
  ]


}
```