#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-cspmioastreamingevent"
  ExtractionType = json
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [""""eventType":"CSPMIOAStreamingEvent"""", """"PolicyStatement":""", """"CloudProvider":"""]
  Fields = [
    """exa_json_path=$.event.EventCreatedTimestamp,exa_field_name=time"""
    """exa_json_path=$.metadata.eventType,exa_field_name=event_category""",
	"""exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$.event.Severity,exa_field_name=alert_severity""",
    """exa_json_path=$.event.UserName,exa_field_name=user"""
    """exa_json_path=$.event.Technique,exa_field_name=alert_type"""
    """exa_json_path=$.event.PolicyStatement,exa_field_name=alert_name"""
    """exa_json_path=$.event.UserSourceIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$.event.Tactic,exa_field_name=category"""
   ]
  

}
```