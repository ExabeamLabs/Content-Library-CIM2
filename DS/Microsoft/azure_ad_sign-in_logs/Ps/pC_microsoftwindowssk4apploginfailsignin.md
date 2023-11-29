#### Parser Content
```Java
{
Name = "microsoft-windows-sk4-app-login-fail-signin"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [ """"OperationName":"Sign-in activity"""", """"Category":"""", """SignInLogs"""", """"ResultType":""" ]
Fields = [
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)""""
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""TIMEGENERATED=({time}\d{4}-\d{1,2}-\d{1,2}\s\d\d:\d\d:\d\d.\d\d\d)""""
""""TIMEGENERATED":"({time}\d{4}-\d{1,2}-\d{1,2}\s\d\d:\d\d:\d\d(\.\d{1,3})?)""""
""""IPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""UserPrincipalName":"({email_address}[^"\s@]+@({email_domain}[^"\s@]+))""""
""""ConditionalAccessStatus":"({result}[^"]+)""""
"""destinationServiceName =\s*({app}[^=]+?)\s+\w+=""",
""""AppDisplayName":"\s*({app}[^"]+?)\s*"""",
"""UserDisplayName"+:"+([a-f\d]+(\-[a-f\d]+){4}|({full_name}[^"]+))"""
"""UserId"+:"+({user_id}[^"]+)"""
""""(Device)?(b|B)rowser":"({browser}[^"]+)"""
""""UserAgent\\*"+:\\*"+(,|({user_agent}[^"]+))"""
""""(Device)?(o|O)peratingSystem":"({os}[^"]+)"""
"""\\*"(F|f)ailureReason\\*":\\*"({failure_reason}.+?)(\.)?\\*""""
]
ParserVersion = "v1.0.0"


}
```