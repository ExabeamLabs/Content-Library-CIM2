#### Parser Content
```Java
{
Name = "microsoft-azure-cef-group-member-remove-success-removefromgroup"
Vendor = "Microsoft"
Product = "Azure AD Activity Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""ActivityDisplayName":"Remove member from group""""
""""OperationName":"Remove"""
""""ActivityDateTime":""""
""""ResourceId":""""
]
Fields = [
"""Group\.DisplayName\\",\\"oldValue\\":\\"\\+"({group_name}[^"\\]+)"""
""""ActivityDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""""
""""InitiatedBy":"\{\\"user\\":\{[^\}]+"userPrincipalName\\":\\"({email_address}[^@"]+@([^\."]+\.[^"]+?)?)\\?""""
""""InitiatedBy":"\{\\"user\\":\{[^\}]+"ipAddress\\":\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\\?""""
""""TenantId":"({account_id}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```