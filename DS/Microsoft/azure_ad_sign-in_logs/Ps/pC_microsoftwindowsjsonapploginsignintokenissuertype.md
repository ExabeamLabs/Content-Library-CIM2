#### Parser Content
```Java
{
Name = "microsoft-windows-json-app-login-signintokenissuertype"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
""""operationName": "Sign-in activity""""
""""conditionalAccessStatus""""
""""tokenIssuerType""""
""""resourceDisplayName": """
""""category": """
"""SignInLogs""""
]
Fields = [
""""time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
"""\d\d:\d\d:\d\d\s({host}[\w\.\-]+)\s\{"time"""",
""""errorCode":\s*({error_code}\d+)""",
""""failureReason":\s*"({failure_reason}[^"]+)"""",
""""Level":\s*({severity}\d+)""",
"""category":\s*"({category}[^"]+)"""",
"""callerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
""""userDisplayName":\s*"({full_name}[^"]+)"""",
""""identity":\s*"({full_name}[^"]+)"""",
""""userPrincipalName":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
""""identity":\s*"({first_name}[^\s"]+)\s({last_name}[^"]+)"""",
""""userId"=:\s*"({user_uid}[^"]+)"""",
""""operationName":\s"({event_name}({operation}[^"]+))"""",
""""userAgent":\s*"({user_agent}[^"]+)"""",
""""authenticationMethod":\s*"({auth_method}[^"]+)"""",
""""conditionalAccessStatus":\s*"({result}[^"]+)"""",
""""tokenIssuerType":\s*"({app}[^"]+)"""",
""""countryOrRegion":\s*"({country_code}[^"]+)"""",
"""deviceDetail\".+?"displayName\":\s*\"({src_host}[\w\-\.]+)\$?\s*\""""
]
ParserVersion = "v1.0.0"


}
```