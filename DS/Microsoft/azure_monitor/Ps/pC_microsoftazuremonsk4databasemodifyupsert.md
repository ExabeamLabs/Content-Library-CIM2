#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-database-modify-upsert
  ParserVersion = v1.0.0
  Conditions=[
    """destinationServiceName =Azure""",
    """"category":"DataPlaneRequests"""",
    """MICROSOFT.DOCUMENTDB""",
    """"operationName":"Upsert""""
  ]

cef-azure-event-hub-cosmosdb = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
     """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
     """clientIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"operationName":"({db_operation}[^"]+)""",
     """"databaseName":"({db_name}[^"]+)""",
     """"collectionName":"({table_name}[^"]+)""",
     """"requestResourceId":"({db_object}[^"]+)""",
     """"callerId":"(Anonymous|({user}[^"]+))""",
     """"userAgent":"({user_agent}[^"]+)""",
     """(?i)({app}MICROSOFT\.DOCUMENTDB)""",
     """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
     """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
     """\[Namespace:\s*({host}\S+) ; EventHub name:"""
     """category":"({category}[^"]+)"""",
     """"resourceId":\s*"({object}[^"]{1,249})"""
  ]
  DupFields = [ "object->resource" 
}
```