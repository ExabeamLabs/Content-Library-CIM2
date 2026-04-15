#### Parser Content
```Java
{
Name = aimsecurity-aisecurity-json-app-policy-violation-aimsecurity
	Vendor = AIM Security
  Product = AI Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
	ExtractionType = json
	Conditions = [ """"payload_type":"app_policy_violation"""", """"event_id":"""", """"policy_name":"""", """"policy_type":"""" ]
	Fields = [
			"""exa_json_path=$.event_timestamp,exa_field_name=time""",
			"""exa_json_path=$.event_id,exa_field_name=event_id""",
			"""exa_json_path=$.payload_type,exa_field_name=event_name""",
			"""exa_json_path=$.policy_name,exa_field_name=policy_name""",
			"""exa_json_path=$.policy_description,exa_field_name=additional_info""",
			"""exa_json_path=$.app,exa_field_name=app""",
			"""exa_json_path=$.severity,exa_field_name=alert_severity""",
			"""exa_json_path=$.user_email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
	]
  ParserVersion = "v1.0.0"


}
```