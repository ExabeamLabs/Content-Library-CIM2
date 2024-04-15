#### Parser Content
```Java
{
Name = "microsoft-azuread-json-app-login-signin"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
"""authenticationMethod"""
"""riskLevelDuringSignIn"""
"""ms:aad:signin"""
"""tokenIssuerType"""
]
Fields = [
""""createdDateTime"+:\s*"+({time}[^"]+)"""
"""ms:aad:signin"+,"+({host}[^"]+)"""
""""userPrincipalName"+:\s*"+({email_address}[^"\s@]+@({email_domain}[^"\s@]+))"""
""""ipAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""userDisplayName"+:\s*"+({full_name}[^"]+)"""
""""failureReason"+:\s*"+(Other|({failure_reason}[^"]+))"""
""""errorCode"+:\s*({error_code}\d+)"""
""""appDisplayName"+:\s*"+({app}[^"]+)"""
""""location"+:\s*\{"+({additional_info}.+?)\},\s*"*servicePrincipalName"""
]
ParserVersion = "v1.0.0"


}
```