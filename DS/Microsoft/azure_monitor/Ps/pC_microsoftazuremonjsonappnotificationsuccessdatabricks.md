#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-notification-success-databricks
  Vendor = Microsoft
  Product = Azure Monitor
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", """yyyy-MM-dd'T'HH:mm:ssZ"""]
  Conditions= [
    """"resourceId":""",
    """"operationName":"Microsoft.Databricks/"""
    """"category":""""
  ]
  Fields =[
  	"""exa_json_path=$.time,exa_field_name=time""",
  	"""exa_regex=({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/"]+)\/RESOURCEGROUPS\/({resource_group}[^\/"]+)(\/PROVIDERS\/({provider_name}[^"]+?))?(\/({resource}[^"\/]+))?)""""
  	"""exa_json_path=$.operationName,exa_field_name=operation""",
  	"""exa_json_path=$.Host,exa_field_name=host""",
  	"""exa_json_path=$.category,exa_field_name=category""",
  	"""exa_json_path=$..sessionId,exa_regex=(null|({session_id}[^"]+))$""",
  	"""exa_json_path=$..serviceName,exa_regex=(null|({service_name}[^"]+))$""",
  	"""exa_json_path=$..userAgent,exa_regex=(null|({user_agent}[^"]+))$""",
  	"""exa_json_path=$..actionName,exa_field_name=action""",
  	"""exa_json_path=$..sourceIPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+)(:({src_port}\d+))?""",
  	"""exa_regex=UserName\\?":\\?"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
  	"""exa_regex=({app}Databricks)"""
  ]


}
```