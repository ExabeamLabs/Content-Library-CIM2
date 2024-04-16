#### Parser Content
```Java
{
Name = "microsoft-azure-cef-group-member-remove-success-removefromgroup"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
ExtractionType = json
Conditions = [
""""ActivityDisplayName":"Remove member from group""""
""""OperationName":"Remove"""
""""ActivityDateTime":""""
""""ResourceId":""""
]
Fields = [
"""Group\.DisplayName\\",\\"oldValue\\":\\"\\+"({group_name}[^"\\]+)"""
"""time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)"""
""""ActivityDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""""
"""targetResources":.+?userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(,|")"""
""""InitiatedBy":"\{\\"user\\":\{[^\}]+"userPrincipalName\\":\\"({email_address}[^@"]+@([^\."]+\.[^"]+?)?)\\?""""
"""callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""InitiatedBy":"\{\\"user\\":\{[^\}]+"ipAddress\\":\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\\?""""
""""TenantId":"({account_id}[^"]+)"""
"""targetResources":.+?id":"({user_uid}[^",]+)"""
"""result":"(notEnabled|notApplied|({result}[^",]+))"""
"""operationName":"({operation}[^",]+)"""
"""({event_name}Remove member from group)"""
"""targetResources":.+?Group\.DisplayName.+?newValue":"\\*"({group_name}[^\\"]+)"""
"""loggedByService":"({app}[^",]+)"""
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\dZ)""""
"""exa_regex=Group\.DisplayName\\",\\"oldValue\\":\\"\\+"({group_name}[^"\\]+)"""
"""exa_json_path=$.time,exa_field_name=time"""
"""exa_regex=targetResources":.+?userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(,|")"""
"""exa_regex="InitiatedBy":"\{\\"user\\":\{[^\}]+"userPrincipalName\\":\\"({email_address}[^@"]+@([^\."]+\.[^"]+?)?)\\?""""
"""exa_json_path=$.callerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""exa_regex=targetResources":.+?Group\.DisplayName.+?newValue":"\\*"({group_name}[^\\"]+)"""
"""exa_regex="TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\dZ)""""
"""exa_regex=targetResources":.+?id":"({user_uid}[^",]+)"""
"""exa_json_path=$.TenantId,exa_field_name=account_id"""
"""exa_json_path=$.properties.result,exa_field_name=result"""
"""exa_regex=({event_name}Remove member from group)"""
"""exa_regex=loggedByService":"({app}[^",]+)"""
"""exa_json_path=$.operationName,exa_field_name=operation"""
"""exa_json_path=$.tenantId,exa_field_name=account_id"""
"""exa_json_path=$.ActivityDisplayName,exa_field_name=operation"""
"""exa_json_path=$.Result,exa_field_name=result"""
]
ParserVersion = "v1.0.0"


}
```