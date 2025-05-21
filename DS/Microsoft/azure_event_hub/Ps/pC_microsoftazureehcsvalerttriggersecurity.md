#### Parser Content
```Java
{
Name = microsoft-azureeh-csv-alert-trigger-security
  ParserVersion = "v1.0.0"
  Product = Azure Event Hub
  Conditions = [ """destinationServiceName =Azure""", """"category":"Security""" ]
  Fields = ${LMSMSParsersTemplates.cef-microsoft-app-activity1.Fields}[
    """\W(ext_properties_eventProperties_userName|ext_properties_eventProperties_accountsUsedOnFailedSignInToHostAttempts_1_)=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """"properties".*?"eventProperties".*?"accountsUsedOnFailedSignInToHostAttempts":\[?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"properties".*?"eventProperties".*?"userName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """\Wext_properties_eventProperties_compromisedEntity=(|({user_upn}.+?))(\s+\w+=|\s*$)""",
    """"properties".*?"eventProperties".*?"compromisedEntity":"({user_upn}[^"]+)"""",
    """\Wext_properties_eventProperties_clientIPAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"properties".*?"eventProperties".*?"clientIPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\Wext_properties_eventProperties_attackers_0_=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"properties".*?"eventProperties".*?"attackers":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
# azure_client_geo_location is removed
# azure_client_geo_location is removed
# azure_alert_event is removed
# azure_alert_event is removed
    """\Wext_properties_eventProperties_attackedResourceType=(|({azure_resource_type}.+?))(\s+\w+=|\s*$)""",
    """"properties".*?"eventProperties".*?"attackedResourceType":"({azure_resource_type}[^"]+)"""",
# malware is removed
# malware is removed
    """\Wext_properties_eventProperties_severity=(|({severity}.+?))(\s+\w+=|\s*$)""",
    """"properties".*?"eventProperties".*?"severity":"({severity}[^"]+)"""",
# client_location is removed
# client_location is removed
    """\Wext_properties_operationId=(|({alert_id}.+?))(\s+\w+=|\s*$)""",
    """\Wext_properties_eventProperties_previousIPAddress=(|({last_known_ip}.+?))(\s+\w+=|\s*$)""",
    """"properties".*?"eventProperties".*?"previousIPAddress":"({last_known_ip}[^"]+)"""",
# failed_login_attempts is removed
# failed_login_attempts is removed
  ]

cef-microsoft-app-activity1 = {
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(.\d{1,7})?Z)"""",
    """"time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w\-.]+ """,
    """"Host":"({host}[^"]+)"""",
    """\WdestinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
    """"message":"({additional_info}[^"]+)""",
    """"description":"({additional_info}[^"]+)""",
    """(?i)category(Value)?":"({category}[^"]+)"""",
    """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """"\_?(R|r)esourceId":\s*"({object}[^"]{1,249})""",
    """"(R|r)esourceId":\s*"({object}[^"]{1,249})""",
    """"(?i)operationName(Value)?":"({operation}[^"]+)""",
    """"name":"({full_name}[^"]+)"""",
    """action":"({action}[^"]+)""",
    """"((?i)callerIpAddress|CIp)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"Caller":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """claims\/(name|upn)":\s*"({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)""",
    """"email":"({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)""",
    """({app}Databricks)""",
    """"serviceName\\*":\\*"({app}[^"]+)""",
    """"sourceIPAddress":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:(\d+))?""", #dl field removed
    """"userAgent":"({user_agent}[^"]+)"""",
    """"statusCode\\":({result_code}\d+)""",
    """"actionName":"({operation}[^"]+)""",
    """userId":"(({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)|({user_id}[^"]+))""",
    """\[Namespace:\s*({host}\S+) ; EventHub name:""",
    """"subscriptionId":"({subscription_id}[^"]+)"""",
    """"ResourceGroup":"({resource_group}[^"]+)""",
    """"\_?(R|r)esourceId":\s*"({resource_id}[^"]+)""",
    """"\_?(R|r)esourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""",
    """"(R|r)esourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""",
    """"LogicalServerName":"({server_name}[^",]+)""",
    """"level"\s*:\s*"({severity}[^"]+)""",
    """"location"\s*:\s*"({location}[^"]+)""""
    """exa_json_path=$.TimeGenerated,exa_field_name=time""",
    """exa_regex="subscriptionId":"({subscription_id}[^"]+)"""",
    """exa_regex=ResourceGroup":"({resource_group}[^"]+)""",
    """exa_regex="\_?(R|r)esourceId":\s*"({resource_id}[^"]+)""",
    """exa_regex="LogicalServerName":"({server_name}[^",]+)""",
    """exa_regex="level"\s*:\s*"({severity}[^"]+)""",
    """exa_regex="location"\s*:\s*"({location}[^"]+)""""
    """exa_regex="message":"({additional_info}[^"]+)""",
    """exa_regex="description":"({additional_info}[^"]+)""",
    """exa_regex=(?i)category(value)?":"({category}[^"]+)"""",
    """exa_regex=Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
    """exa_regex=EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
    """exa_regex="\_?(R|r)esourceId":\s*"({object}[^"]{1,249})""",
    """exa_regex="(R|r)esourceId":\s*"({object}[^"]{1,249})""",
    """exa_regex="(?i)operationName(Value)?":"({operation}[^"]+)"""
    """exa_regex="Host":"({host}[^"]+)"""",
    """exa_regex=\[Namespace:\s*({host}\S+) ; EventHub name:""",
    """exa_regex="\_?(R|r)esourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""",
    """exa_regex="(R|r)esourceId":\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""",
    """exa_json_path=$.Caller,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    ]
  DupFields = [ "object->resource" 
}
```