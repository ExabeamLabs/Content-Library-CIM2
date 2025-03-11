#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-database-modify-success-sql
  Product = Azure Monitor
  Conditions = [ """"resourceId":""", """"EventName":"UpdateDatabase"""", """Microsoft.Sql""", """"operationName":""" ]
  Fields = ${LMSMSParsersTemplates.cef-microsoft-app-activity-3.Fields}[
	""""operationName":\s*\{[^\}]*?"localizedValue":\s*"({db_operation}[^"]+)"""",
	"""request=({result}[^=\s]+)\s+\w+=""",
	"""sourceServiceName =\s*({service_name}[^=]+)\s+\w+=""",
	"""suser=(Azure Security Center|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=""",
	"""\srequestClientApplication=({app}[^=]+)\s+\w+="""
	""""correlationId":"({correlation_id}[^"]+)"""
	""""category":\s*\{[^\}]*?"localizedValue":\s*"({category}[^"]+)""""
  """"Description_scrubbed":"({additional_info}[^=",]+)""""
  """"resourceId":"[^"]+?\/DATABASES\/({db_name}[^\/"]+)""""
  ]
  ParserVersion = "v1.0.0"

cef-microsoft-app-activity-3 = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "M/dd/yyyy hh:mm:ss a Z", "MM/dd/yyyy hh:mm:ss a Z", "MM/dd/yyyy h:mm:ss Z", "M/dd/yyyy h:mm:ss Z", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """"time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"Host":\s*"({host}[\w\-.]+)"""",
    """destinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
    """"message":\s*"({additional_info}[^"]+)""",
    """"description":\s*"({additional_info}[^"]+)""",
    """category":\s*"({category}[^"]+)"""",
    """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """"(?i)resourceId":\s*"({object}[^"]{1,249})""",
    """"operationName":\s*"({operation}[^"]+)""",
    """"name":\s*"({full_name}[^"]+)"""",
    """action":\s*"({action}[^"]+)""",
    """"IPAddress\\?"+\s*:\s*\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"MacAddress\\?"+\s*:\s*\\?"({src_mac}([a-fA-F\d]{0,2}[-:]){0,5}[a-fA-F\d]+)""",
    """"((?i)callerIpAddress|CIp)"*:\s*"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """claims\/(name|upn)":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"email":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """duser=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """({app}Databricks)""",
    """"serviceName\\*":\s*\\*"({app}[^"]+)""",
    # port is removed
    """"userAgent":\s*"({user_agent}[^"]+)"""",
    """"statusCode\\":\s*({result_code}\d+)""",
    """"actionName":\s*"({operation}[^"]+)""",
    """userId":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))""",
    """\[Namespace:\s*({host}\S+) ; EventHub name:"""
    """"subscriptionId":\s*"({subscription_id}[^"]+)"""",
    """"ResourceGroup":\s*"({resource_group}[^"]+)""",
    """"resourceId":\s*"({resource_id}[^"]+)""",
    """"LogicalServerName":\s*"({server_name}[^",]+)""",
    """"UserType":\s*"*({user_type}[^,\}"]+)"*""",
    """"tenantId"\s*:\s*"({tenant_id}[^",]+)""",
    """"level"\s*:\s*"({severity}[^",]+)""",
    """Location"\s*:\s*"({location}[^"]+)""",
    """"resourceId"\s*:\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)\/[^"]+)""""
    """exa_json_path=$.category,exa_field_name=category"""
    """exa_json_path=$.EventTimeString,exa_field_name=time"""
    """exa_json_path=$.EventName,exa_field_name=event_name"""
    """exa_json_path=$.resourceId,exa_field_name=object"""
    """exa_regex=Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """exa_regex=EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """exa_json_path=$.SubscriptionId,exa_field_name=subscription_id"""
    """exa_regex="resourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)\/[^"]+)""""
    """"CorrelationId":\s*"({correlation_id}[^"]+)""""
    ]
  DupFields = [ "object->resource" 
}
```