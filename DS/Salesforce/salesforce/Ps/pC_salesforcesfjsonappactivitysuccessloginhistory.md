#### Parser Content
```Java
{
Name = "salesforce-sf-json-app-activity-success-loginhistory"
  Vendor = "Salesforce"
  Product = "Salesforce"
  ExtractionType = json
  TimeFormat = "yyyyMMddHHmmss.SSS"
  Conditions = [ """"EVENT_TYPE":"""", """"ENTITY_NAME":"""", """"API_TYPE":"""", """"REQUEST_ID":"""", """LoginHistory""" ]
  Fields = [
  	"""exa_json_path=$.EVENT_TYPE,exa_field_name=event_category""",
  	"""exa_json_path=$.REQUEST_ID,exa_field_name=transaction_id""",
  	"""exa_json_path=$.TIMESTAMP,exa_field_name=time""",
  	"""exa_json_path=$.SESSION_KEY,exa_field_name=session_id""",
  	"""exa_json_path=$.METHOD_NAME,exa_regex=(9999|({operation}[^"]+))$""",
  	"""exa_json_path=$.CLIENT_IP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  	"""exa_json_path=$.ENTITY_NAME,exa_field_name=object""",
  	"""exa_json_path=$.USER_NAME,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  	"""exa_json_path=$.USER_ID,exa_field_name=user_id""",
  	"""exa_json_path=$.USER_TYPE,exa_regex=(\d+\.\d+\.\d+\.\d+|({user_type}[^"]+))$""",
  	"""exa_json_path=$.REQUEST_SIZE,exa_field_name=bytes"""
  ]
  ParserVersion = "v1.0.0"


}
```