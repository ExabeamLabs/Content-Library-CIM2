#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-alert-trigger-success-dlppolicymatch"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Microsoft Defender for Endpoint"
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSZ" , "yyyy-MM-dd'T'HH:mm:ssZ" , "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  ExtractionType = "json"
  Conditions = [
    """"serviceSource": "MicrosoftEndPointDlp"""",
    """"detectionSource": "DLP"""",
    """"category": "Exfiltration""""
  ]
  Fields = [
    """exa_json_path=$.incidentId,exa_field_name=alert_id""",
    """exa_json_path=$.alertId,exa_field_name=alert_id""",
    """exa_json_path=$.creationTime,exa_field_name=time""",
    """exa_json_path=$.title,exa_field_name=alert_name""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.status,exa_field_name=alert_status""",
    """exa_json_path=$.detectionSource,exa_field_name=alert_source"""
  ]


}
```