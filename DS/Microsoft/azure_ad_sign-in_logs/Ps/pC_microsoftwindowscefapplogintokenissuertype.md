#### Parser Content
```Java
{
Name = "microsoft-windows-cef-app-login-tokenissuertype"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
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
""""userPrincipalName"+:\s*"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
""""conditionalAccessStatus"+:\s*"+({result}[^"]+)""""
""""tokenIssuerType"+:\s*"+({app}[^"]+)""""
""""failureReason"+:\s*"+({failure_reason}[^"]+?)(\.)?""""
""""status":\s*\{[^\}]*?"errorCode":\s*(0|({failure_code}\d+))(,|\})"""
""""browser"+:\s*"+({browser}[^"]+)""""
""""operatingSystem"+:\s*"+({os}[^"]+)""""
""""userAgent"+:\s*"+({user_agent}[^"]+)\s*""""
""""operationName"+:\s*"+({event_name}[^",]+)"""
""""authenticationMethod":\s*"({auth_method}[^"]+)""""
""""additionalDetails":\s*"({additional_info}[^"]+)""""
""""countryOrRegion":\s*"({country_code}[^"]+)""""
""""resourceId":\s*"({resource}[^"]+)""""
""""(app|resource)DisplayName":\s*"({resource}[^"]+)""""
""""resultType":\s*"({error_code}\d+)""""
"""deviceDetail\".+?"displayName\":\"({src_host}[\w\-\.]+)\$?\s*\""""
"""userId":\s*"({user_id}[^"]+)""""
""""riskDetail":[^,]+,"({additional_info}[^\]]+),"riskEventTypes""""
""""riskLevelAggregated":\s*"(none|({severity}[^"]+))""""
""""category":\s*"({category}[^"]+)""""
"""exa_json_path=$.time,exa_field_name=time""",
"""exa_json_path=$.callerIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
"""exa_json_path=$.identity,exa_regex=(({user_id}\w+-\w+-\w+-\w+-\w+)|({full_name}({last_name}[^",\s]+)\s*,?\s*({first_name}[^",]+)))""",
"""exa_json_path=$..userPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
"""exa_json_path=$..conditionalAccessStatus,exa_field_name=result""",
"""exa_json_path=$..tokenIssuerType,exa_field_name=app""",
"""exa_json_path=$..status.failureReason,exa_field_name=failure_reason""",
"""exa_regex="browser"+:"+({browser}[^"]+)""""
"""exa_json_path=$..deviceDetail.operatingSystem,exa_field_name=os""",
"""exa_json_path=$..userAgent,exa_field_name=user_agent""",
"""exa_json_path=$.operationName,exa_field_name=event_name""",
"""exa_json_path=$..authenticationDetails[:1].authenticationMethod,exa_field_name=auth_method""",
"""exa_regex="additionalDetails":"({additional_info}[^"]+)"""",
"""exa_regex="countryOrRegion":"({country_code}[^"]+)"""",
"""exa_json_path=$..appDisplayName,exa_field_name=resource""",
"""exa_json_path=$.resultType,exa_field_name=error_code""",
"""exa_regex=deviceDetail\".+?"displayName\":\"({src_host}[\w\-\.]+)\$?\s*\""""
"""exa_json_path=$..userId,exa_field_name=user_id""",
"""exa_regex="riskDetail":[^,]+,"({additional_info}[^\]]+),"riskEventTypes""""
"""exa_json_path=$.category,exa_field_name=category"""
"""exa_json_path=$..riskLevelAggregated,exa_field_name=severity,exa_match_expr=!Contains($..riskLevelAggregated,"none")"""
"""exa_regex="status":\s*\{[^\}]*?"errorCode":\s*(0|({failure_code}\d+))(,|\})"""
]
ParserVersion = "v1.0.0"


}
```