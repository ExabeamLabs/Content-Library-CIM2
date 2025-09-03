#### Parser Content
```Java
{
Name = "salesforce-sf-json-app-activity-success-loginhistory"
  Vendor = "Salesforce"
  Product = "Salesforce"
  ExtractionType = json
  TimeFormat = "yyyyMMddHHmmss.SSS"
  Conditions = [ """"EVENT_TYPE":"""", """"ORGANIZATION_ID":"""", """"USER_ID":"""", """"REQUEST_ID":"""" ]
  Fields = [
  	"""exa_json_path=$.EVENT_TYPE,exa_field_name=event_category""",
  	"""exa_json_path=$.REQUEST_ID,exa_field_name=transaction_id""",
  	"""exa_json_path=$.TIMESTAMP,exa_field_name=time""",
  	"""exa_json_path=$.SESSION_KEY,exa_field_name=session_id""",
  	"""exa_json_path=$.METHOD_NAME,exa_regex=(9999|({operation}[^"]+))$""",
  	"""exa_json_path=$.CLIENT_IP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  	"""exa_json_path=$.ENTITY_NAME,exa_field_name=object""",
  	"""exa_json_path=$.USER_NAME,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  	"""exa_json_path=$.USER_ID,exa_field_name=user_id""",
  	"""exa_json_path=$.USER_TYPE,exa_regex=(\d+\.\d+\.\d+\.\d+|({user_type}[^"]+))$""",
  	"""exa_json_path=$.REQUEST_SIZE,exa_field_name=bytes_out"""
    """exa_json_path=$.RESPONSE_SIZE,exa_field_name=bytes_in"""
	  """exa_json_path=$.URI,exa_field_name=url""",
	  """exa_json_path=$.STATUS_CODE,exa_field_name=http_response_code""",
    """exa_json_path=$.REQUEST_STATUS,exa_field_name=state""",
    """exa_json_path=$.METHOD,exa_field_name=method""",
    """exa_json_path=$.SESSION_KEY,exa_field_name=session_id""",
    """exa_json_path=$.API_RESOURCE,exa_field_name=resource_name""",
    """exa_json_path=$.HTTP_METHOD,exa_field_name=method""",
    """exa_json_path=$.CLIENT_NAME,exa_regex=(\\"\\"|({client_name}[^"]+))""",
    """exa_json_path=$.USER_AGENT,exa_regex=(9999|({user_agent}[^"]+))""",
    """exa_json_path=$.ACTION_MESSAGE,exa_field_name=additional_info""",
    """exa_json_path=$.DOCUMENT_ID,exa_field_name=doc_id""",
    """exa_json_path=$.SHARING_PERMISSION,exa_field_name=permission""",
    """exa_json_path=$.SHARING_OPERATION,exa_regex=(9999|({operation}[^"]+))$""",
    """exa_json_path=$.FILE_TYPE,exa_regex=(UNKNOWN|({file_type}[^"]+))""",
    """exa_json_path=$.SIZE_BYTES,exa_field_name=bytes""",
    """exa_json_path=$.DML_TYPE,exa_regex=(9999|({operation}[^"]+))$""",
    """exa_json_path=$.APP_NAME,exa_field_name=app""",
    """exa_json_path=$.CONNECTION_TYPE,exa_field_name=connection_type""",
    """exa_json_path=$.OS_NAME,exa_field_name=os""",
    """exa_json_path=$.CLIENT_GEO,exa_field_name=src_location""", 
    """exa_json_path=$.DEVICE_MODEL,exa_field_name=device_model""",
    """exa_json_path=$.PAGE_URL,exa_field_name=url""",
    """exa_json_path=$.OS_VERSION,exa_field_name=os_version""",
    """exa_json_path=$.BROWSER_NAME,exa_field_name=browser""",
    """exa_json_path=$.DEVICE_ID,exa_field_name=device_id""",
    """exa_json_path=$.CIPHER_SUITE,exa_field_name=cipher""",
    """exa_json_path=$.LOGIN_TYPE,exa_field_name=login_type_text""",
    """exa_json_path=$.SOURCE_IP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.TLS_PROTOCOL,exa_field_name=protocol""",
    """exa_json_path=$.LOGIN_STATUS,exa_field_name=result""",
    """exa_json_path=$.RESPONSE_STATUS,exa_field_name=http_response_code""",
    """exa_json_path=$.REFERRER_URI,exa_field_name=referrer"""
  ]
  ParserVersion = "v1.0.0"


}
```