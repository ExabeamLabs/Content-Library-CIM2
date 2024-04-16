#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-alert-trigger-success-reconnotification
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = "epoch"
  Conditions = [ """"eventType":"ReconNotificationSummaryEvent"""", """"Highlights":["""", """"customerIDString":"""" ]
  Fields = [
    """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
    """exa_json_path=$.event.RuleId,exa_field_name=alert_id""",
    """exa_json_path=$.metadata.eventType,exa_field_name=alert_type""",
    """exa_json_path=$.event.RulePriority,exa_field_name=alert_severity""",
    """exa_json_path=$.event.Highlights[:1],exa_field_name=additional_info"""
  ]
  ParserVersion = "v1.0.0"


}
```