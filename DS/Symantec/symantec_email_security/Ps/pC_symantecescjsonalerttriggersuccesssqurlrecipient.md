#### Parser Content
```Java
{
Name = "symantec-esc-json-alert-trigger-success-squrlrecipient"
ExtractionType = json
Vendor = "Symantec"
Product = "Symantec Email Security"
TimeFormat = "epoch"
Conditions = [ """"eventType": """", """"squrlClickerIp": """", """"squrlRecipient": """", """"severity": """", """"url": """" ]
Fields = [
  """exa_json_path=$.meta.timestamp_ms,exa_field_name=time"""
  """exa_json_path=$.clicktimeInfo.squrlRecipient,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.clicktimeInfo.url,exa_field_name=malware_url"""
  """exa_json_path=$.incident.severity,exa_field_name=alert_severity"""
  """exa_json_path=$.incident.action,exa_field_name=action"""
  """exa_json_path=$.clicktimeInfo.squrlClickerIp,exa_field_name=dest_ip"""
  """exa_json_path=$.meta.eventType,exa_field_name=alert_name"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```