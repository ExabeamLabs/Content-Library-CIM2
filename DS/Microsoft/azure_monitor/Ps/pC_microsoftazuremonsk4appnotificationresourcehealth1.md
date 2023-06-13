#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-notification-resourcehealth-1
  Product = Azure Monitor
  Conditions = [ """destinationServiceName =Azure""", """Microsoft.Resourcehealth""", """dproc=Activity Log""" ]
  Fields = ${LMSMSParsersTemplates.cef-microsoft-app-activity.Fields}[
	""""operationName":\s*\{[^\}]*?"localizedValue":\s*"({operation}[^"]+)"""",
	"""request=({result}[^=\s]+)\s+\w+=""",
	"""sourceServiceName =\s*({service_name}[^=]+)\s+\w+=""",
	"""suser=(Azure Security Center|({user}[^=]+))\s+\w+=""",
	"""\srequestClientApplication=({app}[^=]+)\s+\w+="""
	""""correlationId":"({correlation_id}[^"]+)"""
	""""category":\s*\{[^\}]*?"localizedValue":\s*"({category}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"

cef-microsoft-app-activity = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"Host":"({host}[^"]+)"""",
    """"message":"({additional_info}[^"]+)""",
    """"description":"({additional_info}[^"]+)""",
    """category":"({category}[^"]+)"""",
    """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """"resourceId":\s*"({object}[^"]+)""",
    """"operationName":"({operation}[^"]+)""",
    """"name":"({full_name}[^"]+)"""",
    """action":"({action}[^"]+)""",
    """"((?i)callerIpAddress|CIp)":"({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))(:({src_port}\d+))?"""",
    """claims\/(name|upn)":\s*"({email_address}[^@]+@[^"]+)""",
    """"email":"({email_address}[^\s@"]+@[^\s@"]+)""",
    """({app}Databricks)""",
    """"serviceName\\*":\\*"({app}[^"]+)""",
    """\WdestinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
# port is removed
    """"userAgent":"({user_agent}[^"]+)"""",
    """"statusCode\\":({http_response_code}\d+)""",
    """"actionName":"({operation}[^"]+)""",
    """userId":"(({email_address}[^@"]+@[^"]+)|({user_id}[^"]+))""",
    """\[Namespace:\s*({host}\S+) ; EventHub name:"""
    ]
  DupFields = [ "object->resource" 
}
```