#### Parser Content
```Java
{
Name = "microsoft-azure-json-app-login-userdisplayname"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
Conditions = [
""""operationName": "Sign-in activity""""
"""appDisplayName":"""
"""userDisplayName"""
]
Fields = [
"""time"*:\s"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""
"""tenantId"*:\s"*({host}[^\s"]+)""""
"""errorCode"*:({error_code}\d+)"""
"""failureReason"*:"*({failure_reason}[^"]+)""""
""""Level"*:\s*({severity}\d+)"""
"""category"*:\s*"*({category}[^"]+)""""
"""callerIpAddress"*:\s*"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""appDisplayName"*:"*({app}[^"]+)""""
""""+identity"+:\s*"+({full_name}[^"]+)"""
"""userPrincipalName"*:"*({email_address}[^@"\s]+?@({email_domain}[^"\s]+?))""""
""""+identity"+:\s*"+({first_name}[^\s"]+)\s({last_name}[^"]+)""""
"""userId"*:"*({user_uid}[^"]+)""""
"""operationName"*:\s"*({operation}[^"]+)""""
"""userAgent"*:"*({user_agent}[^"]+)""""
"""deviceDetail.+?displayName"*:\s*"*({object}[^"]+)""""
"""authenticationMethod"*:"*({auth_method}[^"]+)""""
""""+location"+:(\{"+geoCoordinates"+:\{\}\}|({additional_info}\{.*?\}))"""
""""+result"+:"+({result}[^"]+)"+"""
]
ParserVersion = "v1.0.0"


}
```