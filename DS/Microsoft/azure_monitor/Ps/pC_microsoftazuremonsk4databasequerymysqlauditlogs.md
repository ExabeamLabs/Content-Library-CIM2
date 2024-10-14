#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-database-query-mysqlauditlogs
  Product = Azure Monitor
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"MySqlAuditLogs"""",
    """"event_class":"general_log""""
  ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-db-for-mysql.Fields} [
    """"sql_text":"({db_query}.+?)"*\}\}\s+""",
    """"error_code":({error_code}\d+)""",
    """"thread_id":({thread_id}\d+)"""
    """destinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
  ]

cef-azure-db-for-mysql = {
   Vendor = Microsoft
   TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
   Fields = [
     """"LogicalServerName":"({server_name}[^",]+)""",
     """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
     """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z)""",
     """"user":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
     """"resourceId":"({resource}[^",]+)""",
     """"event_subclass":"({action}[^",]+)""",
     """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"ResourceGroup":"({server_group}[^"]+)""",
     """"SubscriptionId":"({subscription_id}[^"]+)""",
# resource_provider is removed
     """"category":"({category}[^"]+)""",
     """"operationName":"({action}[^"]+)""",
     """\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
     """"resourceId":"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?\/[^"]+)"""",
     """exa_json_path=$.time,exa_field_name=time""",
     """exa_json_path=$.StartTime,exa_field_name=time""",
     """exa_json_path=$.resourceId,exa_field_name=resource""",
     """exa_json_path=$.category,exa_field_name=category""",
     """exa_json_path=$.operationName,exa_field_name=action""",
     """exa_json_path=$.operationName,exa_field_name=action""",
     """exa_regex=Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
     """exa_regex=EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
     """exa_regex="resourceId":"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?\/[^"]+)""""
   ]
   DupFields = ["action->operation","event_hub_namespace->host", "resource->object"
}
```