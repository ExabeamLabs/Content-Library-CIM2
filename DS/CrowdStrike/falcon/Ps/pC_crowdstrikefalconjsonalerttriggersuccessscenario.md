#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-alert-trigger-success-scenario
    Vendor = CrowdStrike
    Product = Falcon
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """"scenario":"""", """"detection_id":""", """"tactic":"""", """"technique":""""]
    Fields = [
      """exa_json_path=$.behaviors[:1].scenario,exa_field_name=alert_name""",
		  """exa_json_path=$.behaviors[:1].technique,exa_field_name=alert_type""",
  		"""exa_json_path=$.behaviors[:1].severity,exa_field_name=alert_severity""",
	  	"""exa_json_path=$.detection_id,exa_field_name=alert_id""",
		  """exa_json_path=$.behaviors[:1].user_name,exa_field_name=user""",
  		"""exa_json_path=$.behaviors[:1].timestamp,exa_field_name=time""",
	  	"""exa_json_path=$.behaviors[:1].md5,exa_regex=(N\/A|({hash_md5}\w+))""",
		  """exa_json_path=$.device.local_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  		"""exa_json_path=$.device.machine_domain,exa_field_name=domain""",
	  	"""exa_json_path=$.behaviors[:1].filename,exa_field_name=process_name""",
		  """exa_json_path=$.device.hostname,exa_field_name=src_host""",
  		"""exa_regex="show_in_ui":.*?"status":"({result}[^"]+)""",
	  	"""exa_json_path=$.status,exa_field_name=result""",
		  """exa_json_path=$.behaviors[:1].cmdline,exa_field_name=additional_info""",
  		"""exa_json_path=$.behaviors[:1].tactic,exa_field_name=category""",
	  	"""exa_regex="((?i)SHA256|SHA256String|SHA256HashData)\\*"+:\s*\\*"+({hash_sha256}[^,]+?)\\*"+,""",
		  """exa_regex="(?i)Quarantine_File"+:\s*({quarantine_file}true|false)""",
      """exa_regex="(?i)Quarantine_Machine"+:\s*({quarantine_machine}true|false)""",
      """exa_regex="(?i)Detect"+:\s*({detect}true|false)""",
      """exa_regex="(?i)Registry_Operation_Blocked"+:\s*({registry_operation_blocked}true|false)""",
      """exa_regex="(?i)Kill_Parent"+:\s*({kill_parent}true|false)""",
      """exa_regex="(?i)Operation_Blocked"+:\s*({operation_blocked}true|false)""",
      """exa_regex="(?i)Kill_Process"+:\s*({kill_process}true|false)""",
      """exa_regex="(?i)Process_Blocked"+:\s*({process_blocked}true|false)""",
      """exa_regex="(?i)Policy_Disabled"+:\s*({policy_disabled}true|false)""",
      """exa_regex="(?i)Sensor_Only"+:\s*({sensor_only}true|false)""",
      """exa_regex="(?i)Kill_SubProcess"+:\s*({kill_sub_process}true|false)""",
      """exa_regex="(?i)Rooting"+:\s*({rooting}true|false)""",
      """exa_regex="(?i)Inddet_Mask"+:\s*({inddet_mask}true|false)""",
      """exa_regex="(?i)Indicator"+:\s*({indicator}true|false)""",
      """exa_json_path=$.cid,exa_field_name=cid""",
		  """exa_json_path=$.device.platform_name,exa_field_name=os"""
    ]
    DupFields = [ "src_host->host" ]
 ParserVersion = "v1.0.0"


}
```