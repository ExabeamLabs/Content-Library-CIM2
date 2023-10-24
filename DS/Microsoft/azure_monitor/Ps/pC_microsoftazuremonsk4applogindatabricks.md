#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-login-databricks
  Conditions= [ """"resourceId":""", """operationName":"Microsoft.Databricks/ssh/login""" ]
  ParserVersion = "v1.0.0"

cef-microsoft-app-activity = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"Host":"({host}[^"]+)"""",
    """\WdestinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
    """"message":"({additional_info}[^"]+)""",
    """"description":"({additional_info}[^"]+)""",
    """category":"({category}[^"]+)"""",
    """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """"resourceId":\s*"({object}[^"]{1,249})""",
    """"operationName":"({operation}[^"]+)""",
    """"name":"({full_name}[^"]+)"""",
    """action":"({action}[^"]+)""",
    """"((?i)callerIpAddress|CIp)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """claims\/(name|upn)":\s*"({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)""",
    """"email":"({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)""",
    """({app}Databricks)""",
    """"serviceName\\*":\\*"({app}[^"]+)""",
    """"sourceIPAddress":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:(\d+))?""", #dl field removed
    """"userAgent":"({user_agent}[^"]+)"""",
    """"statusCode\\":({result_code}\d+)""",
    """"actionName":"({operation}[^"]+)""",
    """userId":"(({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)|({user_id}[^"]+))""",
    """\[Namespace:\s*({host}\S+) ; EventHub name:"""
    ]
  DupFields = [ "object->resource" 
}
```