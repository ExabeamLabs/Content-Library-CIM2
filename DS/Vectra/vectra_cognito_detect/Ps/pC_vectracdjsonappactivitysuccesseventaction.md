#### Parser Content
```Java
{
Name = vectra-cd-json-app-activity-success-eventaction
  Vendor = Vectra
  Product = Vectra Cognito Detect
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"api_client_id":""", """"event_action":""", """"event_object":""", """"result_status":""" ]
  Fields =[
  	"""exa_json_path=$..event_timestamp,exa_field_name=time""",
  	"""exa_json_path=$..message,exa_field_name=event_name""",
  	"""exa_json_path=$..source_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  	"""exa_json_path=$..user_role,exa_field_name=role""",
  	"""exa_json_path=$..event_action,exa_field_name=operation""",
  	"""exa_json_path=$..user_type,exa_field_name=user_type""",
  	"""exa_json_path=$..user_id,exa_field_name=user_id""",
  	"""exa_json_path=$..result_status,exa_field_name=result""",
  	"""exa_json_path=$..event_object,exa_field_name=event_category""",
  	"""exa_json_path=$..username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  	"""exa_json_path=$..event_data,exa_field_name=additional_info""",
  	"""exa_json_path=$..event_data,exa_field_name=event_id"""
  ]
  ParserVersion = "v1.0.0"
 

}
```