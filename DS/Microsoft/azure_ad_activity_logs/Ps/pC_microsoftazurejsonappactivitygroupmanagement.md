#### Parser Content
```Java
{
Name = microsoft-azure-json-app-activity-groupmanagement
  Conditions= [ """"category":"GroupManagement"""", """"operationName":"Add owner to group"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}GroupManagement)"""
    """exa_regex=({category}GroupManagement)"""
    """Group\.ObjectID\\"[^\}]+?"newValue\\":\\"\\+"({object}[^"\\]+)"""
    """exa_regex=Group\.ObjectID\\"[^\}]+?"newValue\\":\\"\\+"({object}[^"\\]+)"""
  ]
  ParserVersion = "v1.0.0"

ms-azure-eventhubs-activity = {
  Vendor = Microsoft
  Product = Azure AD Activity Logs
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Fields = [
    """"ActivityDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)"""",
    """"ActivityDisplayName":"({event_name}[^"]+)"""",
    """"ResourceId":"({object}[^"]+)"""",
    """"resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""""
    """"value\\":\\"({user_agent}[^"]+?)\\?",\\"key\\":\\"User-Agent\\"""",
    """"key\\":\\"User-Agent\\",\\"value\\":\\"({user_agent}[^"]+?)\\?"""",
    """(?i)"+callerIpAddress"+:"+(<null>|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+""",
    """"+initiatedBy.*?"+userPrincipalName\\?"+:\\?"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"+"""
    """TargetResources":"\[[^|]+userPrincipalName\\":\\"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))\\?"""",
    """"+targetResources.*?"+displayName"+:"+({object}[^"]+?)"+""",
    """"+targetResources.*?"+userPrincipalName"+:"+({object}[^"]+?)"+"""
    """"targetResources":\[\{[^\}]+\},\{"displayName"[^\]]+?\.DisplayName","newValue":"\\?"({target}[^"\\]+)"""
    """"+time"+:"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}\w+)"+"""
    """"+operationName"+:"+({operation}[^"]+)"+""",
    """(?i)"+result"+:"+({result}[^"]+)"+""",
    """Category":"({category}[^"]+)""",
    """"Type":"({event_category}[^"]+)""",
    """"type":"({additional_info}[^"]+)""",
    """"Resource":"({resource}[^"]+)""",
    """destinationServiceName =({app}Azure)""",
    """({app}eventHubsAzureRecord)""",
    """({app}eventhubbeat_APL_Azure)""",
    """"app"+:\{[^\}]*?displayName"+:"+({app}[^",]+)"""",
    """object=({object}[^\|=\s]+)(\||\s\w+=)"""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\dZ)""""
    """exa_json_path=$.ActivityDateTime,exa_field_name=time"""
    """exa_json_path=$.ActivityDisplayName,exa_field_name=event_name"""
    """exa_json_path=$.ResourceId,exa_field_name=object"""
    """exa_regex=resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""""
    """exa_regex="key\\":\\"User-Agent\\",\\"value\\":\\"({user_agent}[^"]+?)\\?"""",
    """exa_regex=(?i)"+callerIpAddress"+:"+(<null>|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+""",
    """exa_regex="+initiatedBy.*?"+userPrincipalName\\?"+:\\?"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"+"""
    """exa_regex=TargetResources":"\[[^|]+userPrincipalName\\":\\"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))\\?"""",
    """exa_regex="+targetResources.*?"+displayName"+:"+({object}[^"]+?)"+""",
    """exa_regex="+targetResources.*?"+userPrincipalName"+:"+({object}[^"]+?)"+"""
    """exa_regex="targetResources":\[\{[^\}]+\},\{"displayName"[^\]]+?\.DisplayName","newValue":"\\?"({target}[^"\\]+)"""
    """exa_json_path=$.operationName,exa_field_name=operation"""
    """exa_json_path=$.Category,exa_field_name=category"""
    """exa_json_path=$.Type,exa_field_name=event_category"""
    """exa_regex="type":"({additional_info}[^"]+)""",
    """exa_json_path=$.Resource,exa_field_name=resource"""
    """exa_regex=destinationServiceName =({app}Azure)""",
    """exa_regex=({app}eventHubsAzureRecord)""",
    """exa_regex=({app}eventhubbeat_APL_Azure)""",
    """exa_regex="app"+:\{[^\}]*?displayName"+:"+({app}[^",]+)"""",
    """exa_regex=object=({object}[^\|=\s]+)(\||\s\w+=)"""
    """exa_regex=(?i)"+result"+:"+({result}[^"]+)"+""",
    """exa_json_path=$.TimeGenerated,exa_field_name=time"""
  ]
  DupFields = [ "event_name->operation" 
}
```