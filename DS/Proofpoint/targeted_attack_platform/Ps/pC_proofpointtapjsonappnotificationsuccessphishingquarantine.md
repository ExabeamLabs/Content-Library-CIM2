#### Parser Content
```Java
{
Name = proofpoint-tap-json-app-notification-success-phishingquarantine
  ParserVersion = v1.0.0
  Conditions = [ """"proofpoint_trap"""","""Phishing""", """"quarantine_results":"""]
 
proofpoint-tap-log = {
  Vendor = Proofpoint
  Product = Targeted Attack Platform
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSZ"
  Fields = [
  """exa_json_path=$.event.description.incident_id,exa_field_name=alert_id""", 
	"""exa_json_path=$.event.description.sender,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""", 
	"""exa_json_path=$.event.description.classification,exa_field_name=classification_name""", 
	"""exa_json_path=$.event.description.messageid,exa_field_name=message_id""", 
	"""exa_json_path=$.event.description.recipient,exa_regex=({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\\*"\]""", 
	"""exa_json_path=$.event.description.subject,exa_field_name=email_subject""", 
	"""exa_json_path=$.event.overwrite,exa_field_name=result""", 
	"""exa_json_path=$.event.description.custom_data_static,exa_field_name=product_name"""
  """exa_json_path=$.event.description.alertId,exa_field_name=alert_id""",
  """exa_json_path=$.event.description.quarantine_results[0].alertSource,exa_field_name=alert_source""",
  """exa_json_path=$.event.description.quarantine_results[0].alertId,exa_field_name=alert_id""",
  """exa_json_path=$.event.description.quarantine_results[0].status,exa_field_name=alert_status""",
  ]
 
}
```