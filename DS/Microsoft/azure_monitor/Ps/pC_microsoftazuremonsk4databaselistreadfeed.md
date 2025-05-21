#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-database-list-readfeed
  ParserVersion = v1.0.0
  Conditions=[
    """"resourceId":""",
    """"category":"DataPlaneRequests"""",
    """MICROSOFT.DOCUMENTDB""",
    """"operationName":"ReadFeed""""
  ]

cef-azure-event-hub-cosmosdb = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
     """"TimeGenerated":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
     """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
     """clientIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"operationName":\s*"({db_operation}[^"]+)""",
     """"databaseName":\s*"({db_name}[^"]+)""",
     """"collectionName":\s*"({table_name}[^"]+)""",
     """"requestResourceId":\s*"({db_object}[^"]+)""",
     """"callerId":\s*"(Anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
     """"userAgent":\s*"({user_agent}[^"]+)""",
     """(?i)({app}MICROSOFT\.DOCUMENTDB)""",
     """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
     """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
     """\[Namespace:\s*({host}\S+) ; EventHub name:"""
     """category":\s*"({category}[^"]+)"""",
     """"resourceId":\s*"({object}[^"]{1,249})"""
     """"_?ResourceId":\s*"({resource_id}[^"]+)""""
     """"SubscriptionId":\s*"({subscription_id}[^"]+)""""
  ]
  DupFields = [ "object->resource" 
}
```