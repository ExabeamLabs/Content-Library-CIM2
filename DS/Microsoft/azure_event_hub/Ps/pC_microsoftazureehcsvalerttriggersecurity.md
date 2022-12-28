#### Parser Content
```Java
{
Name = microsoft-azureeh-csv-alert-trigger-security
  ParserVersion = "v1.0.0"
  Product = Azure Event Hub
  Conditions = [ """destinationServiceName =Azure""", """"category":"Security""" ]
  Fields = ${LMSMSParsersTemplates.cef-microsoft-app-activity.Fields}[
    """\W(ext_properties_eventProperties_userName|ext_properties_eventProperties_accountsUsedOnFailedSignInToHostAttempts_1_)=(|({user}.+?))(\s+\w+=|\s*$)""",
    """"properties".*?"eventProperties".*?"accountsUsedOnFailedSignInToHostAttempts":\[?"({user}[^"]+)"""",
    """"properties".*?"eventProperties".*?"userName":"({user}[^"]+)"""",
    """\Wext_properties_eventProperties_compromisedEntity=(|({user_upn}.+?))(\s+\w+=|\s*$)""",
    """"properties".*?"eventProperties".*?"compromisedEntity":"({user_upn}[^"]+)"""",
    """\Wext_properties_eventProperties_clientIPAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"properties".*?"eventProperties".*?"clientIPAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\Wext_properties_eventProperties_attackers_0_=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"properties".*?"eventProperties".*?"attackers":\["({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
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
    """"((?i)callerIpAddress|CIp)":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
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