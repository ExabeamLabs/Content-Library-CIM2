#### Parser Content
```Java
{
Name = microsoft-azuremon-json-alert-trigger-success-cputhresholdexceeded
  Vendor = Microsoft
  Product = Azure Monitor
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"Type":"Alert"""", """"AlertName":"""", """"AlertSeverity":"""", """"AlertRuleInstanceId":"""", """"SourceSystem":"OMS"""" ]
  Fields = [
    """exa_json_path=$.TimeGenerated,exa_field_name=time""",
    """exa_json_path=$.Computer,exa_field_name=host""",
    """exa_json_path=$.AlertName,exa_field_name=alert_name""",
    """exa_json_path=$.AlertSeverity,exa_field_name=alert_severity""",
    """exa_json_path=$.Type,exa_field_name=alert_type""",
    """exa_json_path=$.AlertDescription,exa_field_name=additional_info""",
  ]
  ParserVersion = v1.0.0


}
```