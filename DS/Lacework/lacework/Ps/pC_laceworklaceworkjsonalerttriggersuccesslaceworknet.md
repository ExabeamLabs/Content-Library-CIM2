#### Parser Content
```Java
{
Name = "lacework-lacework-json-alert-trigger-success-laceworknet"
ExtractionType = json
Vendor = "Lacework"
Product = "Lacework"
TimeFormat = "dd MMM yyyy HH:mm z"
Conditions = [ """lacework_account""", """lacework.net""", """event_title""", """event_source""" ]
Fields = [
"""exa_json_path=$.event_type,exa_field_name=alert_type"""
"""exa_json_path=$.event_timestamp,exa_field_name=time"""
"""exa_json_path=$.event_severity,exa_field_name=alert_severity"""
"""exa_json_path=$.event_source,exa_field_name=alert_source"""
"""exa_json_path=$.event_title,exa_field_name=alert_name"""
"""exa_json_path=$.event_id,exa_field_name=alert_id"""
"""exa_json_path=$.event_link,exa_field_name=link"""
"""exa_json_path=$.event_description,exa_regex=\s*({alert_description}[^"]+?)"""
"""exa_json_path=$.lacework_account,exa_field_name=account"""
]
ParserVersion = "v1.0.0"


}
```