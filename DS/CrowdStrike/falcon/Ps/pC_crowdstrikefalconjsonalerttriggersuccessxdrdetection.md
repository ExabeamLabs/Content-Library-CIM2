#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-xdrdetection"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
ParserVersion = "v1.0.0"
TimeFormat = ["epoch_sec","epoch"]
Conditions = [ """"eventType":"XdrDetectionSummaryEvent"""", """"Tactics":"""", """"Techniques":"""" ]
Fields = [
  """exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
	"""exa_json_path=$.metadata.eventType,exa_field_name=event_category""",
	"""exa_json_path=$.destinationServiceName,exa_field_name=app""",
	"""exa_json_path=$.event.Description,exa_field_name=additional_info""",
	"""exa_json_path=$.event.Severity,exa_field_name=alert_severity""",
	"""exa_json_path=$.event.DetectId,exa_field_name=alert_id""",
	"""exa_json_path=$.event.Tactics,exa_field_name=category""",
	"""exa_json_path=$.event.Techniques,exa_field_name=alert_name""",
	"""exa_json_path=$.event.Users,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?<!local)""",
	"""exa_json_path=$.event.Name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?<!local)""",
	"""exa_json_path=$.event.DomainNames,exa_regex=({domain}[^,]+)""",
	"""exa_json_path=$.event.IPv4Addresses,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
	"""exa_regex="HostNames":"({host}[^,]+)"""
  """exa_json_path=$..cid,exa_field_name=cid""",
  """exa_json_path=$..customerIDString,exa_field_name=cid"""
]
DupFields = [ "category->alert_type" ]


}
```