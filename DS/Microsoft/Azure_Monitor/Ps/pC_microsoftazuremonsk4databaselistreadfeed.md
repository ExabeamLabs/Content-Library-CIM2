#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-database-list-readfeed
  ParserVersion = v1.0.0
  Conditions=[
    """destinationServiceName =Azure""",
    """"category":"DataPlaneRequests"""",
    """MICROSOFT.DOCUMENTDB""",
    """"operationName":"ReadFeed""""
  ]

cef-azure-event-hub-cosmosdb = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
     """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
     """clientIpAddress":"({src_ip}[^"]+)""",
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
  
}
```