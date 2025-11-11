#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-updatenamespace
  ExtractionType = json
  ParserVersion = v1.0.0
  Conditions= [ """"EventName":"Update Namespace"""", """"category":"OperationalLogs"""" ]

cef-microsoft-app-activity-3 = {
  Vendor = Microsoft
  Product = Azure Monitor
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "M/dd/yyyy hh:mm:ss a Z", "MM/dd/yyyy hh:mm:ss a Z", "MM/dd/yyyy h:mm:ss Z", "M/dd/yyyy h:mm:ss Z", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """"time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"Host":\s*"({host}[\w\-.]+)"""",
    """destinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
    """"message":\s*"({failure_reason}({additional_info}[^"]+))""",
    """"description":\s*"({failure_reason}({additional_info}[^"]+))""",
    """category":\s*"({category}[^"]+)"""",
    """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """"(?i)resourceId":\s*"({resource}({object}[^"]{1,249}))""",
    """"operationName":\s*"({operation}[^"]+)""",
    """action":\s*"({action}[^"]+)""",
    """"IPAddress\\?"+\s*:\s*\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"MacAddress\\?"+\s*:\s*\\?"({src_mac}([a-fA-F\d]{0,2}[-:]){0,5}[a-fA-F\d]+)""",
    """"((?i)callerIpAddress|CIp)"*:\s*"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
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
    """exa_regex=Location"\s*:\s*"({location}[^"]+)""",
    """"resourceId"\s*:\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)\/[^"]+)""""
    """"_?ResourceId":\s*"({resource_id}[^"]+)""""
    """exa_json_path=$.._ResourceId,exa_field_name=resource_id"""
    """exa_json_path=$.category,exa_field_name=category"""
    """exa_json_path=$.EventTimeString,exa_field_name=time"""
    """exa_json_path=$.EventName,exa_field_name=event_name"""
    """exa_regex=Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """exa_regex=EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """exa_json_path=$..SubscriptionId,exa_field_name=subscription_id"""
    """exa_regex="resourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)\/[^"]+)""""
    """"CorrelationId":\s*"({correlation_id}[^"]+)""""

    """exa_json_path=$.time,exa_field_name=time"""
    """exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """
    """exa_json_path=$..Host,exa_field_name=host"""
    """exa_regex=destinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
    """exa_json_path=$..message,exa_field_name=event_name"""
    """exa_json_path=$..description,exa_field_name=additional_info"""
    """exa_json_path=$..description,exa_field_name=failure_reason"""
    """exa_regex=category":\s*"({category}[^"]+)"""",
    """exa_regex=Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """exa_regex=EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """exa_regex=(?i)resourceId":\s*"({resource}({object}[^"]{1,249}))""",
    """exa_regex="operationName":\s*"({operation}[^"]+)"""
    """exa_json_path=$..action,exa_field_name=action"""
    """exa_regex=IPAddress\\?"+\s*:\s*\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex=MacAddress\\?"+\s*:\s*\\?"({src_mac}([a-fA-F\d]{0,2}[-:]){0,5}[a-fA-F\d]+)""",
    """exa_regex=((?i)callerIpAddress|CIp)"*:\s*"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex=claims\/(name|upn)":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_regex=email":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_regex=duser=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_regex=({app}Databricks)""",
    """exa_regex=serviceName\\*":\s*\\*"({app}[^"]+)""",
    """exa_json_path=$..userAgent,exa_field_name=user_agent"""
    """exa_json_path=$..statusCode,exa_field_name=result_code"""
    """exa_regex="actionName":\s*"({operation}[^"]+)"""
    """exa_regex=userId":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))""",
    """exa_regex=\[Namespace:\s*({host}\S+) ; EventHub name:"""
    """exa_json_path=$..ResourceGroup,exa_field_name=resource_group"""
    """exa_regex=resourceId":\s*"({resource_id}[^"]+)"""
    """exa_json_path=$..LogicalServerName,exa_field_name=server_name"""
    """exa_json_path=$..UserType,exa_field_name=user_type"""
    """exa_regex="tenantId"\s*:\s*"({tenant_id}[^",]+)"""
    """exa_json_path=$..level,exa_field_name=severity"""
    """exa_json_path=$..location,exa_field_name=location"""
    """exa_regex="CorrelationId":\s*"({correlation_id}[^"]+)""""
    """exa_regex=message":\s*"({failure_reason}({additional_info}[^"]+))""",
    
}
```