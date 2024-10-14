#### Parser Content
```Java
{
Name = "microsoft-azure-json-app-login-azurerecord"
Conditions = [
"""eventHubsAzureRecord"""
"""Sign-in activity"""
]
ParserVersion = "v1.0.0"

cef-azure-event-hub-1.Fields}[
"""\"application_name\":\"({app}[^\"]+)\""""
"""\"statement\":\"({db_query}[^\"]+)\""""
"""\"database_name\":\"({db_name}[^\"]+)\""""
"""\"schema_name\":\"({db_schema}[^\"]+)\""""
"""\"server_principal_name\":\"({server_group}[^\"]+)\""""
"""\"client_ip\":\"({src_ip}[A-Fa-f\d\.:]+)\""""
"""\"additional_information\":\"({additional_info}[^\"]+)\""""
]  
},

${MicrosoftAzureParsersTemplates.cef-azure-event-hub-1}{
  Name = microsoft-azure-sk4-alert-trigger-success-security
  ParserVersion = v1.0.0
  Conditions = [ """"category":"Security"""", """"eventName"""", """"operationName":"""" ]
  Fields = ${MicrosoftAzureParsersTemplates.cef-azure-event-hub-1.Fields}[
    """"compromisedHost":"({dest_host}[\w\-.]+)"""",
    """compromisedEntity":"({user_upn}[^"]+)"""",
    """userName":"(({domain}[^\\"]+)\\+)?(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\(]+)\s*)""",
    """clientIPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """severity":"({alert_severity}[^"]+)"""",
    """operationId":"({alert_id}[^"]+)"""",
    """category":"({azure_category}[^"]+)"""",
    """attackedResourceType":"({azure_resource_type}[^"]+)"""",
    """eventName":"({alert_type}[^"\\]+)[\\]*"""",
    """"(detail|result)Description":"({additional_info}[^"]+)[\\]*"""",
    """"resourceId":"({resource}[^"]+)"""",
    """"resourceId":"[^"]*\/RESOURCEGROUPS\/({account_id}[^\/]+)\/""",
    """"correlationId":"({correlation_id}[^"]+)"""",
    """"operationName":"({operation}[^"]+)""""
  ]
  DupFields = ["alert_type->alert_name"
}
```