#### Parser Content
```Java
{
Name = "microsoft-azuread-json-group-member-add-success-aadiam"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
"""Microsoft.aadiam"""
"""Add member to group"""
"""tenantId":""""
]
Fields = [
"""time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)"""
"""initiatedBy":.+?userPrincipalName":"({email_address}[^",]+)"""
"""initiatedBy":.+?id":"({user_uid}[^",]+)"""
"""callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""operationName":"({operation}[^",]+)"""
"""result":"(notEnabled|notApplied|({result}[^",]+))"""
"""category":"({category}[^",]+)"*,correlationId""""
""""app":\{.*?displayName":"({app}[^",]+)"""
"""loggedByService":"({app}[^",]+)"""
"""({event_name}Add member to group)"""
"""targetResources"+:\[\{([^,]+,){3}"+userPrincipalName"+:"+({dest_user}[^"]+)""""
"""targetResources"+:\[\{[^\}]+\

}
```