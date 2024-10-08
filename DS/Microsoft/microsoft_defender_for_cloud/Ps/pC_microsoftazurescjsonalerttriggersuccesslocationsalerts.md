#### Parser Content
```Java
{
Name = microsoft-azuresc-json-alert-trigger-success-locationsalerts
  Vendor = Microsoft
  Product = Microsoft Defender for Cloud
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"type":""", """"Microsoft.Security/Locations/alerts"""", """"productName":""", """"Microsoft Defender for Cloud"""", """"alertDisplayName":""" ]
  Fields = [
    """exa_json_path=$.properties.startTimeUtc,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exa_json_path=$.properties.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.properties.alertDisplayName,exa_field_name=alert_name""",
    """exa_json_path=$.properties.alertType,exa_field_name=alert_type""",
    """exa_json_path=$.properties.systemAlertId,exa_field_name=alert_id""",
    """exa_json_path=$.type,exa_field_name=operation""",
    """exa_json_path=$.properties.description,exa_field_name=additional_info""",
    """exa_json_path=$..resourceId,exa_field_name=resource""",
    """exa_json_path=$.properties.alertUri,exa_field_name=uri"""
  ]
  ParserVersion = v1.0.0


}
```