#### Parser Content
```Java
{
Name = "microsoft-windows-cef-app-login-conditionalaccessstatus"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""OperationName":"Sign-in activity""""
""""ConditionalAccessStatus":""""
]
Fields = [
"""\"TimeGenerated\":\"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
"""\"IPAddress\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\""""
"""\"UserPrincipalName\":\"({email_address}[^\"\s@]+@({email_domain}[^\"\s@]+))\""""
"""\"ConditionalAccessStatus\":\"({result}[^\"]+)\""""
"""destinationServiceName =({app}[^=]+?)\s+\w+="""
"""\"AppDisplayName\":\"({app}[^\"]+)"""
"""UserDisplayName\"+:\"+({full_name}[^\"]+)"""
"""UserId\"+:\"+({user_id}[^\"]+)"""
"""\"+IPAddress\"+:\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"UserAgent\\*\"+:\\*\"+({user_agent}[^\"]+)"""
"""src-application-name\"+:\"+({app}[^\"]+)"""
"""\"failureReason\":\"({failure_reason}.+?)(\.)?\""""
]
ParserVersion = "v1.0.0"


}
```