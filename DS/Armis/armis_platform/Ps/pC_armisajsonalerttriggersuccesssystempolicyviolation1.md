#### Parser Content
```Java
{
Name = armis-a-json-alert-trigger-success-systempolicyviolation-1
  ParserVersion = v1.0.0
  Vendor = Armis
  Product = Armis Platform
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  ExtractionType = json
  Conditions = [  """"activities": """, """"status": """, """"type": "SYSTEM_POLICY_VIOLATION"""",""""severity":""",   ]
  Fields = [
    """exa_json_path=$._time,exa_field_name=time""",
    """exa_json_path=$.title,exa_field_name=alert_name""",
    """exa_regex=({alert_type}SYSTEM_POLICY_VIOLATION)""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.status,exa_field_name=sub_status""",
    """exa_json_path=$.description,exa_field_name=additional_info""",
	  """exa_json_path=$.riskLevel,exa_field_name=risk_level""",
	  """exa_json_path=$.policy.owner,exa_field_name=owner_id""",
	  """exa_json_path=$.policy.actionParams.alertDescription,exa_field_name=alert_description"""
	  """exa_json_path=$.hostname,exa_field_name=host""",
    """exa_regex="user":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """exa_json_path=$..sourceEndpoints[*].ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    ]


}
```