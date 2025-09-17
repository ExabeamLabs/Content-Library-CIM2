#### Parser Content
```Java
{
Name = google-agentspace-json-app-activity-success-agentspace
    ExtractionType = json
    Vendor = Google
    Product = Google Agentspace
    ParserVersion = "v1.0.0"
    TimeFormat = [ """yyyy-MM-dd'T'HH:mm:ss.SSSZ""" ]
    Conditions = [ """"methodName":""", """"serviceLabel":""", """"serviceName":""", """"google.cloud.discoveryengine.""" ]
    Fields = [
		"""exa_json_path=$.ts,exa_field_name=time""", 
		"""exa_json_path=$.serviceName,exa_field_name=service_name""", 
		"""exa_json_path=$.methodName,exa_field_name=event_name""", 
		"""exa_json_path=$.serviceLabel,exa_field_name=service_type""", 
		"""exa_json_path=$.user,exa_regex=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@,\s:]+))?)""", 
		"""exa_json_path=$.query,exa_field_name=query""", 
		"""exa_json_path=$.request.name,exa_field_name=resource""", 
		"""exa_json_path=$.request.query.parts[0].text,exa_field_name=additional_info""", 
		"""exa_json_path=$.response.answer.state,exa_field_name=state""", 
		"""exa_json_path=$.response.assistToken,exa_field_name=identifier""", 
		"""exa_json_path=$.response.answer.name,exa_field_name=response""", 
		"""exa_json_path=$.request.userInfo.userId,exa_field_name=user_id""", 
		"""exa_json_path=$.user,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""" 
    ]


}
```