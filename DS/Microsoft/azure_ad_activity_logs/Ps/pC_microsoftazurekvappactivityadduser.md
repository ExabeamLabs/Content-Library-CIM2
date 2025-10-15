#### Parser Content
```Java
{
Name = microsoft-azure-kv-app-activity-adduser
  Conditions = [ """"category":""", """"UserManagement"""", """"operationName":""", """"Add user"""", """"activityDisplayName"""" ]
  Fields = ${MSParsersTemplates.ms-azure-eventhubs-activity.Fields}[
    """({category}UserManagement)"""
    """exa_regex=({category}UserManagement)"""
  ]
  ParserVersion = "v1.0.0"

ms-azure-eventhubs-activity = {
  Vendor = Microsoft
  Product = Azure AD Activity Logs
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Fields = [
    """"ActivityDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
    """"ActivityDisplayName":\s*"({event_name}[^"]+)"""",
    """"ResourceId":\s*"({object}[^"]+)"""",
    """"resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""""
    """"value\\":\s*\\"({user_agent}[^"]+?)\\?",\\"key\\":\s*\\"User-Agent\\"""",
    """"key\\":\s*\\"User-Agent\\",\\"value\\":\s*\\"({user_agent}[^"]+?)\\?"""",
    """(?i)"+callerIpAddress"+:\s*"+(<null>|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+""",
    """"+initiatedBy.*?"+userPrincipalName\\?"+:\s*\\?"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"+"""
    """TargetResources":\s*"\[[^|]+userPrincipalName\\":\s*\\"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """"+targetResources.*?"+displayName"+:\s*"+({object}[^"]+?)"+""",
    """"+targetResources.*?"+userPrincipalName"+:\s*"+({object}[^"]+?)"+"""
    """"targetResources":\s*\[\{[^\}]+\},\{"displayName"[^\]]+?\.DisplayName","newValue":\s*"\\?"({target}[^"\\]+)"""
    """"+time"+:\s*"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}\w+)"+"""
    """"+operationName"+:\s*"+({operation}[^"]+)"+""",
    """(?i)"+result"+:\s*"+({result}[^"]+)"+""",
    """Category":\s*"({category}[^"]+)""",
    """"Type":\s*"({event_category}[^"]+)""",
    """"type":\s*"({additional_info}[^"]+)""",
    """"Resource":\s*"({resource}[^"]+)""",
    """destinationServiceName =({app}Azure)""",
    """({app}eventHubsAzureRecord)""",
    """({app}eventhubbeat_APL_Azure)""",
    """"app"+:\s*\{[^\}]*?displayName"+:\s*"+({app}[^",]+)"""",
    """object=({object}[^\|=\s]+)(\||\s\w+=)"""
    """"TimeGenerated":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\dZ)""""
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.ActivityDateTime,exa_field_name=time"""
    """exa_json_path=$.ActivityDisplayName,exa_field_name=event_name"""
    """exa_json_path=$.ResourceId,exa_field_name=object"""
    """exa_regex=resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""""
    """exa_regex="key\\":\s*\\"User-Agent\\",\\"value\\":\s*\\"({user_agent}[^"]+?)\\?"""",
    """exa_regex=(?i)"+callerIpAddress"+:\s*"+(<null>|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+""",
    """exa_regex="+initiatedBy.*?"+userPrincipalName\\?"+:\s*\\?"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"+"""
    """exa_regex=TargetResources":\s*"\[[^|]+userPrincipalName\\":\s*\\"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"""",
    """exa_regex="+targetResources.*?"+displayName"+:\s*"+({object}[^"]+?)"+""",
    """exa_regex="+targetResources.*?"+userPrincipalName"+:\s*"+({object}[^"]+?)"+"""
    """exa_regex="targetResources":\s*\[\{[^\}]+\},\{"displayName"[^\]]+?\.DisplayName","newValue":\s*"\\?"({target}[^"\\]+)"""
    """exa_json_path=$.operationName,exa_field_name=operation"""
    """exa_json_path=$.Category,exa_field_name=category"""
    """exa_json_path=$.Type,exa_field_name=event_category"""
    """exa_regex="type":\s*"({additional_info}[^"]+)""",
    """exa_json_path=$.Resource,exa_field_name=resource"""
    """exa_regex=destinationServiceName =({app}Azure)""",
    """exa_regex=({app}eventHubsAzureRecord)""",
    """exa_regex=({app}eventhubbeat_APL_Azure)""",
    """exa_regex="app"+:\s*\{[^\}]*?displayName"+:\s*"+({app}[^",]+)"""",
    """exa_regex=object=({object}[^\|=\s]+)(\||\s\w+=)"""
    """exa_regex=(?i)"+result"+:\s*"+({result}[^"]+)"+""",
    """exa_json_path=$.TimeGenerated,exa_field_name=time"""
    """TargetResources":"\[.+?"displayName\\":\\"Group.DisplayName\\",.+?\\"newValue\\":\\"\\*"({group_name}[^"\\]+)"""
    """Group\.DisplayName\\[^}]+"newValue\\":\s*[\\"]+({group_name}[^"\\]+)"""
    """TargetResources":"\[.+?"displayName\\":\\"({group_name}[^"\\]+)"""
    """groupType\\":\\"({group_type}[^"\\]+)"""
    """GroupType\\",\\"oldValue\\":\\"\\*({group_type}[^\\\[]+)"""
    """exa_regex=TargetResources":"\[.+?"displayName\\":\\"Group.DisplayName\\",.+?\\"newValue\\":\\"\\*"({group_name}[^"\\]+)"""
    """exa_regex=Group\.DisplayName\\[^}]+"newValue\\":\s*[\\"]+({group_name}[^"\\]+)"""
    """exa_regex=groupType\\":\\"({group_type}[^"\\]+)"""
    """exa_regex=GroupType\\",\\"oldValue\\":\\"\\*({group_type}[^\\\[]+)"""
   """exa_regex=TargetResources":"\[.+?"displayName\\":\\"({group_name}[^"\\]+)"""
  ]
  DupFields = [ "event_name->operation" 
}
```