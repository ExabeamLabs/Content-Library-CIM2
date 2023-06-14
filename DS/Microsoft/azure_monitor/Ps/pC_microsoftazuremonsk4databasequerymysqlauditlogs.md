#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-database-query-mysqlauditlogs
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """destinationServiceName =Azure""",
    """"category":"MySqlAuditLogs"""",
    """"event_class":"general_log""""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
    """"sql_text":"({db_query}.+?)"*\}\}\s+""",
    """"error_code":({error_code}\d+)""",
    """"thread_id":({thread_id}\d+)"""
    """\WdestinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
  ]

cef-azure-db-for-mysql = {
   Vendor = Microsoft
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
   Fields = [
     """"LogicalServerName":"({host}[^",]+)""",
     """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
     """"user":"({user}[\w\-]+)""",
     """"resourceId":"({resource}[^",]+)""",
     """"event_subclass":"({action}[^",]+)""",
     """"ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"ResourceGroup":"({server_group}[^"]+)""",
     """"SubscriptionId":"({subscription_id}[^"]+)""",
# resource_provider is removed
     """"category":"({category}[^"]+)""",
     """"operationName":"({action}[^"]+)""",
     """\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
   ]
   DupFields = ["action->operation","event_hub_namespace->host", "resource->object"
}
```