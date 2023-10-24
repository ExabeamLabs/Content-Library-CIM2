#### Parser Content
```Java
{
Name = "microsoft-windows-cef-app-login-tokenissuertype"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""operationName""""
""""Sign-in activity""""
""""conditionalAccessStatus""""
""""tokenIssuerType""""
"""":""""
]
Fields = [
""""time"+:\s*"+({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
""""callerIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
""""identity"+:\s*"+(({user_id}\w+-\w+-\w+-\w+-\w+)|({full_name}({last_name}[^",\s]+)\s*,?\s*({first_name}[^",]+)))""""
""""userPrincipalName"+:"+({email_address}[^"\s@]+@[^"\s@]+)""""
""""conditionalAccessStatus"+:"+({result}[^"]+)""""
""""tokenIssuerType"+:"+({app}[^"]+)""""
""""failureReason"+:"+({failure_reason}[^"]+?)(\.)?""""
""""browser"+:"+({browser}[^"]+)""""
""""operatingSystem"+:"+({os}[^"]+)""""
""""userAgent"+:"+({user_agent}[^"]+)\s*""""
""""operationName"+:\s*"+({event_name}[^",]+)"""
""""authenticationMethod":"({auth_method}[^"]+)""""
""""additionalDetails":"({additional_info}[^"]+)""""
""""countryOrRegion":"({country_code}[^"]+)""""
""""appDisplayName":"({resource}[^"]+)""""
""""resultType":\s*"({error_code}\d+)""""
"""deviceDetail":\{[^\}]+?displayName":"({src_host}[^"]+)""""
"""userId":"({user_id}[^"]+)""""
""""riskDetail":[^,]+,"({additional_info}[^\]]+),"riskEventTypes""""
]
ParserVersion = "v1.0.0"


}
```