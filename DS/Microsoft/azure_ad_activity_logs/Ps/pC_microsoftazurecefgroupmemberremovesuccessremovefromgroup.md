#### Parser Content
```Java
{
Name = "microsoft-azure-cef-group-member-remove-success-removefromgroup"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
ExtractionType = json
Conditions = [
""""ActivityDisplayName":"""
""""Remove member from group""""
""""OperationName":"""
""""Remove"""
""""ActivityDateTime":"""
""""ResourceId":"""
]
Fields = [
"""Group\.DisplayName\\",\\"oldValue\\":\s*\\"\\+"({group_name}[^"\\]+)"""
"""time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)"""
""""ActivityDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""""
""""type":"User","userPrincipalName":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(,|")"""
""""InitiatedBy":\s*"\{\\"user\\":\s*\{[^\}]+"userPrincipalName\\":\s*\\"({email_address}[^@"]+@([^\."]+\.[^"]+?)?)\\?""""
"""callerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""InitiatedBy":\s*"\{\\"user\\":\s*\{[^\}]+"ipAddress\\":\s*\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\\?""""
""""TenantId":\s*"({account_id}[^"]+)"""
""""id":\s*"({user_uid}[^",]+)","type":"User""""
"""result":\s*"(notEnabled|notApplied|({result}[^",]+))"""
"""operationName":\s*"({operation}[^",]+)"""
"""({event_name}Remove member from group)"""
"""targetResources":[^\]]+Group\.DisplayName[^\}]+newValue":\s*"\\*"({group_name}[^\\"]+)"""
"""loggedByService":\s*"({app}[^",]+)"""
""""TimeGenerated":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\dZ)""""
"""exa_regex=Group\.DisplayName\\",\\"oldValue\\":\s*\\"\\+"({group_name}[^"\\]+)"""
"""exa_json_path=$.time,exa_field_name=time"""
"""exa_regex="type":"User","userPrincipalName":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(,|")"""
"""exa_regex="InitiatedBy":\s*"\{\\"user\\":\s*\{[^\}]+"userPrincipalName\\":\s*\\"({email_address}[^@"]+@([^\."]+\.[^"]+?)?)\\?""""
"""exa_json_path=$.callerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""exa_regex=targetResources":[^\]]+Group\.DisplayName[^\}]+newValue":\s*"\\*"({group_name}[^\\"]+)"""
"""exa_regex="TimeGenerated":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\dZ)""""
"""exa_regex="id":\s*"({user_uid}[^",]+)","type":"User""""
"""exa_json_path=$.TenantId,exa_field_name=account_id"""
"""exa_json_path=$..result,exa_field_name=result"""
"""exa_regex=({event_name}Remove member from group)"""
"""exa_regex=loggedByService":\s*"({app}[^",]+)"""
"""exa_json_path=$.operationName,exa_field_name=operation"""
"""exa_json_path=$.tenantId,exa_field_name=account_id"""
"""exa_json_path=$.ActivityDisplayName,exa_field_name=operation"""
"""exa_json_path=$.Result,exa_field_name=result"""
]
ParserVersion = "v1.0.0"


}
```