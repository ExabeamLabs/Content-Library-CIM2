#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-auditevent
  Product = Azure Monitor
  Conditions = [ """category":"AuditEvent"""", """MICROSOFT.KEYVAULT""" ]
  Fields = ${LMSMSParsersTemplates.cef-microsoft-app-activity.Fields}[
     """(?i)({app}Microsoft.KeyVault)""",
    """operationName":"({operation}[^"]+)"""",
    """resultSignature":"({result}[^"]+)"""",
    """resourceId":"({resource}[^"]+)"""",
    """requestUri":"({request_uri}[^"]+)"""",
    """callerIpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """resultDescription":"({additional_info}[^"]+)"""",
    """claims\/upn":"({email_address}[^"]+)""",
    """"properties":.+?"id":"({object}[^"]+)"""
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