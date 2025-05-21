#### Parser Content
```Java
{
Name = microsoft-mcas-cef-app-activity-success-mailboxpermission
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Add recipient mailbox permission|"""
]
ParserVersion = "v1.0.0"

ms-azure-eventhubs-activity.Fields}[
    """({category}Device)""",
    """"operationType":\s*"({operation_type}[^",]+)""""
    """exa_regex=({category}Device)""",
    """exa_json_path=$.operationType,exa_field_name=operation_type"""
  ]
  ParserVersion = "v1.0.0"
},

${MSParsersTemplates.ms-azure-eventhubs-activity} {
  Name = microsoft-azure-json-app-activity-updateuser
  Conditions= [ """"category":""", """"UserManagement"""", """"operationName":""", """"Update user"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}UserManagement)""",
    """exa_regex=({category}UserManagement)""",
    """"Resource":\s*"({resource}[^"]+)""",
    """exa_json_path=$.Resource,exa_field_name=resource"""
    """TargetResources":\s*"\[[^|]+userPrincipalName\\":\s*\\"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """exa_regex=TargetResources":\s*"\[[^|]+userPrincipalName\\":\s*\\"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """"ActivityDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)"""",
    """"ResourceId":\s*"({object}[^"]+)"""",
    """"resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""""
    """"InitiatedBy":\s*"\{\\"user\\":\s*\{[^\}]+"userPrincipalName\\":\s*\\"({email_address}[^@"]+@[^\."]+\.[^"]+?)\\?"""",
    """exa_regex="resourceId":\s*\s*"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)"""
    """exa_regex="InitiatedBy":\s*"\{\\"user\\":\s*\{[^\}]+"userPrincipalName\\":\s*\\"({email_address}[^@"]+@[^\."]+\.[^"]+?)\\?"""",
    """"ActivityDisplayName":\s*"({event_name}[^"]+)"""",
    """CallerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"InitiatedBy":\s*"\{\\"user\\":\s*\{[^\}]+"ipAddress\\":\s*\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\\?"""",
    """\\"ipAddress\\":\s*\\"(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\\""""
    """exa_json_path=$.ActivityDateTime,exa_field_name=time"""
    """exa_json_path=$.ResourceId,exa_field_name=object"""
    """exa_json_path=$.ActivityDisplayName,exa_field_name=event_name"""
    """exa_regex=CallerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex="InitiatedBy":\s*"\{\\"user\\":\s*\{[^\}]+"ipAddress\\":\s*\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\\?"""",
    """exa_regex=\\"ipAddress\\":\s*\\"(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\\""""
  ]
  ParserVersion = "v1.0.0"
},

${MSParsersTemplates.azure-app-activity-2}{
  Name = microsoft-azuremon-sk4-app-activity-success-updategroup
  ParserVersion = v1.0.0
  Conditions = [ """"ActivityDisplayName":""", """"Update group"""", """"OperationName":""", """"Update group"""", """"ActivityDateTime":""", """"ResourceId":""" 
}
```