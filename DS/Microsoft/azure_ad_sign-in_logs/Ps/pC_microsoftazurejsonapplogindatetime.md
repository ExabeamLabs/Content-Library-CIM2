#### Parser Content
```Java
{
Name = "microsoft-azure-json-app-login-datetime"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = "epoch"
Conditions = [ """"signinDateTimeInMillis":""", """"loginStatus": """", """"mfaAuthDetail":""" ]
Fields = [
""""signinDateTimeInMillis":\s*({time}\d{13})"""
""""ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""loginStatus":\s*"({result}[^"]+)"""
""""mfaResult":\s*"({additional_info}[^"]+)"""
""""signinErrorCode":\s*({error_code}\d+)"""
""""userDisplayName":\s*"({first_name}[^,"]+),\s*({last_name}[^,"]+)"""
""""appDisplayName":\s*"({app}[^"]+?)\s*""""
""""userPrincipalName":\s*"({email_address}[^\s"@]+@({email_domain}[^\s"@]+))"""
""""failureReason":\s*"*(null|({failure_reason}[^,"]+))"""
]
ParserVersion = "v1.0.0"


}
```