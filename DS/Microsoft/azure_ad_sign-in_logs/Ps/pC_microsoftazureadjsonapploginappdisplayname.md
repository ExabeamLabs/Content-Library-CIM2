#### Parser Content
```Java
{
Name = "microsoft-azuread-json-app-login-appdisplayname"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
""""userDisplayName": """"
""""appDisplayName": """"
""""createdDateTime": """"
]
Fields = [
""""createdDateTime":\s*"({time}[^"]+)"""
""""userPrincipalName":\s*"({email_address}[^"\s@]+@({email_domain}[^"\s@]+))"""
""""ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""userDisplayName":\s*"({last_name}[^,"\(]+?)\s*(\([^\)]*\))?,\s*({first_name}[^"\(]+?)\s*(\([^\)]*\))?""""
""""failureReason":\s*"(Other|({failure_reason}[^"]+))"""
""""errorCode":\s*({error_code}\d+)"""
""""appDisplayName":\s*"({app}[^"]+)"""
""""location":\s*\{"({additional_info}.+?)\},\s*"authenticationRequirementPolicies":"""
]
ParserVersion = "v1.0.0"


}
```