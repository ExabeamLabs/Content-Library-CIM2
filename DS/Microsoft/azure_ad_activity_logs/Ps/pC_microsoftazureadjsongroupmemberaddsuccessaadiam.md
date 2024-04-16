#### Parser Content
```Java
{
Name = "microsoft-azuread-json-group-member-add-success-aadiam"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
ExtractionType = json
Conditions = [
"""Microsoft.aadiam"""
"""Add member to group"""
"""tenantId":""""
]
Fields = [
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)""",
"""time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)"""
""""userPrincipalName(\\)?":(\\)?"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""initiatedBy":.+?userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""initiatedBy":.+?id":"({user_uid}[^",]+)"""
"""callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""operationName":"({operation}[^",]+)"""
"""result":"(notEnabled|notApplied|({result}[^",]+))"""
"""category":"({category}[^",]+)"*,correlationId""""
""""app":\{.*?displayName":"({app}[^",]+)"""
"""loggedByService":"({app}[^",]+)"""
"""({event_name}Add member to group)"""
"""targetResources"+:\[\{([^,]+,){3}"+userPrincipalName"+:"+({dest_user}[^"]+)""""
"""targetResources"+:\[\{[^\}]+\},\{[^:]+:"+Group.DisplayName"+,[^,]+,"+newValue"+:"+\\*"+({group_name}[^\\"]+)"""
"""Group\.DisplayName\\[^}]+"newValue\\":[\\"]+({group_name}[^"\\]+)"""
""""TargetResources":"\[\{\\"id\\":\\"({account_id}[^"\\]+)""",
""""displayName".*?Group\.ObjectID".*?newValue":"\\"?({group_id}[^\\"]+)\\"?""""
""""Category":"({category}[^"]+)""""
"""targetResources"+:\[\{"+id"+:"+({account_id}[^",]+)"""
"""exa_json_path=$.TimeGenerated,exa_field_name=time"""
"""exa_json_path=$.time,exa_field_name=time"""
"""exa_regex="userPrincipalName(\\)?":(\\)?"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""exa_regex=initiatedBy":.+?userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""exa_regex=callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$..initiatedBy.user.id,exa_field_name=user_uid"""
"""exa_json_path=$.operationName,exa_field_name=operation"""
"""exa_regex=result":"(notEnabled|notApplied|({result}[^",]+))"""
"""exa_json_path=$.properties.category,exa_field_name=category"""
"""exa_regex="app":\{.*?displayName":"({app}[^",]+)"""
"""exa_json_path=$.properties.loggedByService,exa_field_name=app"""
"""exa_regex=targetResources"+:\[\{([^,]+,){3}"+userPrincipalName"+:"+({dest_user}[^"]+)""""
"""exa_regex=targetResources"+:\[\{[^\}]+\},\{[^:]+:"+Group.DisplayName"+,[^,]+,"+newValue"+:"+\\*"+({group_name}[^\\"]+)"""
"""exa_regex=Group\.DisplayName\\[^}]+"newValue\\":[\\"]+({group_name}[^"\\]+)"""
"""exa_json_path=$.properties.targetResources[:1].id,exa_field_name=account_id"""
"""exa_regex="displayName".*?Group\.ObjectID".*?newValue":"\\"?({group_id}[^\\"]+)\\"?""""
"""exa_json_path=$.Category,exa_field_name=category"""
]
ParserVersion = "v1.0.0"


}
```