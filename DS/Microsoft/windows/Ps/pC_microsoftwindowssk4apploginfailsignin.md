#### Parser Content
```Java
{
Name = "microsoft-windows-sk4-app-login-fail-signin"
Vendor = "Microsoft"
Product = "Windows"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""OperationName":"Sign-in activity""""
"""destinationServiceName =Azure"""
]
Fields = [
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)""""
""""TIMEGENERATED=({time}\d{4}-\d{1,2}-\d{1,2}\s\d\d:\d\d:\d\d.\d\d\d)""""
""""IPAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""UserPrincipalName":"({email_address}[^"\s@]+@({email_domain}[^"\s@]+))""""
""""ConditionalAccessStatus":"({result}[^"]+)""""
"""\sdestinationServiceName =\s*({app}[^=]+?)\s+\w+=""",
""""AppDisplayName":"\s*({app}[^"]+)\s*"""",
"""UserDisplayName"+:"+([a-f\d]+(\-[a-f\d]+){4}|({full_name}[^"]+))"""
"""UserId"+:"+({user_id}[^"]+)"""
""""+IPAddress"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""(Device)?(b|B)rowser":"({browser}[^"]+)"""
""""UserAgent\\*"+:\\*"+(,|({user_agent}[^"]+))"""
""""(Device)?(o|O)peratingSystem":"({os}[^"]+)"""
""""(F|f)ailureReason":"({failure_reason}.+?)(\.)?""""
]
ParserVersion = "v1.0.0"


}
```