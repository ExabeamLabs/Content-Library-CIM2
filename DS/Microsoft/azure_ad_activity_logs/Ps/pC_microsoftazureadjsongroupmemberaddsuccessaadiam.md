#### Parser Content
```Java
{
Name = "microsoft-azuread-json-group-member-add-success-aadiam"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
ExtractionType = json
Conditions = [ """Microsoft.aadiam""", """Add member to group""", """tenantId":""" ]
Fields = [
""""TimeGenerated":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)""",
"""time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)"""
""""userPrincipalName(\\)?":\s*(\\)?"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""initiatedBy":.+?userPrincipalName":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""initiatedBy":.+?id":\s*"({user_uid}[^",]+)"""
"""callerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""operationName":\s*"({operation}[^",]+)"""
"""result":\s*"(notEnabled|notApplied|({result}[^",]+))"""
"""category":\s*"({category}[^",]+)"*,correlationId""""
""""app":\s*\{.*?displayName":\s*"({app}[^",]+)"""
"""loggedByService":\s*"({app}[^",]+)"""
"""({event_name}Add member to group)"""
"""targetResources"+:\s*\[\{([^,]+,){3}"+userPrincipalName"+:\s*"+({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"\s]+)""""
"""targetResources"+:\s*\[\{[^\}]+\},\{[^:]+:\s*"+Group.DisplayName"+,[^,]+,"+newValue"+:\s*"+\\*"+({group_name}[^\\"]+)"""
"""Group\.DisplayName\\[^}]+"newValue\\":\s*[\\"]+({group_name}[^"\\]+)"""
""""TargetResources":\s*"\[\{\\"id\\":\s*\\"({account_id}[^"\\]+)""",
""""displayName".*?Group\.ObjectID".*?newValue":\s*"\\"?({group_id}[^\\"]+)\\"?""""
""""displayName".*?newValue":\s*"\\"?({group_id}[^\\"]+)\\"?","displayName":"Group.ObjectID""""
""""Category":\s*"({category}[^"]+)""""
"""targetResources"+:\s*\[\{"+id"+:\s*"+({account_id}[^",]+)"""
"""exa_json_path=$.TimeGenerated,exa_field_name=time"""
"""exa_json_path=$.time,exa_field_name=time"""
"""exa_regex="userPrincipalName(\\)?":\s*(\\)?"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""exa_regex=initiatedBy":.+?userPrincipalName":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""exa_regex=callerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$..initiatedBy.user.id,exa_field_name=user_uid"""
"""exa_json_path=$.operationName,exa_field_name=operation"""
"""exa_regex=result":"(notEnabled|notApplied|({result}[^",]+))"""
"""exa_json_path=$.properties.category,exa_field_name=category"""
"""exa_regex="app":\s*\{.*?displayName":\s*"({app}[^",]+)"""
"""exa_json_path=$..loggedByService,exa_field_name=app"""
"""exa_regex=targetResources"+:\s*\[\{([^,]+,){3}"+userPrincipalName"+:\s*"+({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"\s]+)""""
"""exa_regex=targetResources"+:\s*\[\{[^\}]+\},\{[^:]+:\s*"+Group.DisplayName"+,[^,]+,"+newValue"+:\s*"+\\*"+({group_name}[^\\"]+)"""
"""exa_regex=Group\.DisplayName\\[^}]+"newValue\\":\s*[\\"]+({group_name}[^"\\]+)"""
"""exa_json_path=$..targetResources[:1].id,exa_field_name=account_id"""
"""exa_regex="displayName".*?Group\.ObjectID".*?newValue":\s*"\\"?({group_id}[^\\"]+)\\"?""""
"""exa_regex="displayName".*?newValue":\s*"\\"?({group_id}[^\\"]+)\\"?","displayName":"Group.ObjectID""""
"""exa_json_path=$.Category,exa_field_name=category"""
]
ParserVersion = "v1.0.0"


}
```