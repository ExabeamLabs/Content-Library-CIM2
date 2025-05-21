#### Parser Content
```Java
{
Name = zimperium-mtd-json-alert-trigger-success-threatuuid
  Vendor = Zimperium
  Product = Zimperium MTD
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "dd MM yyyy HH:mm:ss z"
  Conditions = [ """"zapp_instance_id":""",""""threat_type":""",""""threat_uuid":""",""""device_info":""" ]
  Fields = [
  """exa_json_path=$.forensics.eventtimestamp,exa_field_name=time"""
	"""exa_json_path=$.forensics.user_info.user_email,exa_regex="({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
	"""exa_json_path=$.forensics.user_info.employee_name,exa_field_name=full_name"""
	"""exa_json_path=$.forensics.threat.general.device_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
	"""exa_json_path=$.severity,exa_regex=({alert_severity}\d{1,5})"""
	"""exa_json_path=$.event_id,exa_field_name=alert_id"""
	"""exa_json_path=$.forensics.threat.story,exa_field_name=additional_info"""
	"""exa_json_path=$.forensics.threat.general.threat_type,exa_field_name=alert_type"""
	"""exa_json_path=$.forensics.general,exa_regex=Threat.+?"name":\s"({alert_name}[^"]+)"""
  ]


}
```