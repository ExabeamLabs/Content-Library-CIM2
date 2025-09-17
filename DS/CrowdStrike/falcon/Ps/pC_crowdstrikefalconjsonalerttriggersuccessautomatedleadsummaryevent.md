#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-automatedleadsummaryevent"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ExtractionType = json
  TimeFormat = ["epoch_sec", "epoch"]
  Conditions = [ """"eventType":""", """"AutomatedLeadSummaryEvent"""", """"FalconHostLink":"""", """"LeadId":""" ]
  Fields = [
    """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
    """exa_json_path=$.metadata.eventType,exa_field_name=alert_type""",
    """exa_json_path=$.event.ThreatgraphIndicators[0].Description,exa_field_name=additional_info""",
    """exa_json_path=$.event.ThreatgraphIndicators[0].IndicatorId,exa_field_name=ioc_number""",
    """exa_json_path=$.event.ThreatgraphIndicators[0].Hostname,exa_field_name=src_host""",
    """exa_json_path=$.event.ThreatgraphIndicators[0].DisplayName,exa_field_name=alert_name""",
    """exa_json_path=$.event.ThreatgraphIndicators[0].Severity,exa_field_name=alert_severity""",
    """exa_json_path=$.event.ThreatgraphIndicators[0].ProcessId,exa_field_name=process_id""",
    """exa_json_path=$.event.MitreAttack[0].Tactic,exa_field_name=tactic""",
    """exa_json_path=$.event.MitreAttack[0].Technique,exa_field_name=technique""",
    """exa_json_path=$.event.MitreAttack[0].PatternID,exa_field_name=threat_id""",
    """exa_json_path=$.event.FalconHostLink,exa_field_name=falcon_host_link"""
  ]
  ParserVersion = "v1.0.0"


}
```