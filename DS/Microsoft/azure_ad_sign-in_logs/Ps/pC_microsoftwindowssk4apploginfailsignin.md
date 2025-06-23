#### Parser Content
```Java
{
Name = "microsoft-windows-sk4-app-login-fail-signin"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSZ", "yyyy-MM-dd HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSZ"]
Conditions = [ """"OperationName":"Sign-in activity"""", """"Category":"""", """SignInLogs"""", """"ResultType":""" ]
Fields = [
""""+time"+:"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}\w+)"+"""
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""
""""TIMEGENERATED=({time}\d{4}-\d{1,2}-\d{1,2}\s\d\d:\d\d:\d\d.\d\d\d)""""
""""TIMEGENERATED":"({time}\d{4}-\d{1,2}-\d{1,2}\s\d\d:\d\d:\d\d(\.\d{1,3})?)""""
""""IPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""UserPrincipalName":"({email_address}[^"\s@]+@({email_domain}[^"\s@]+))""""
""""ConditionalAccessStatus":"({result}[^"]+)""""
"""destinationServiceName =\s*({app}[^=]+?)\s+\w+=""",
""""AppDisplayName":"\s*({app}[^"]+?)\s*"""",
""""identity"+:\s*"+(({user_id}\w+-\w+-\w+-\w+-\w+)|({full_name}[^"]+))""""
"""UserDisplayName"+:"+([a-f\d]+(\-[a-f\d]+){4}|({full_name}[^"]+))"""
"""UserId"+:"+({user_id}[^"]+)"""
""""(Device)?(b|B)rowser":"({browser}[^"]+)"""
""""UserAgent\\*"+:\\*"+(,|({user_agent}[^"]+))"""
""""(Device)?(o|O)peratingSystem":"({os}[^"]+)"""
"""\\*"(F|f)ailureReason\\*":\\*"({failure_reason}.+?)(\.)?\\*""""
"""(?i)status(_string)?\\*":\s*"*\{[^\}]*?\\*"errorCode\\*":\s*(0|({failure_code}\d+))(,|\})"""
""""+operationName"+:"+({operation}[^"]+)"+"""
""""+identity"+:"+({last_name}[^",]+),\s*({first_name}[^",\/]+)(\/[^"]*)?""""
""""riskDetail":[^,]+,"({additional_info}[^\]]+),"riskEventTypes""""
""""geoCoordinates\\*"+:\{(|({location}.+?))\}"""
"""additionalDetails\\*":\s*\\*"({additional_info}[^"\\]+)"""
"""(?i)deviceDetail(_string)?\\*":"?\{[^\}]*"displayName\\*":\\*"({src_host}[\w\-\.]+)\$?\s*\\*"""
"""(?i)deviceDetail(_string)?\\*":"?\{[^\}]*"deviceId\\*":\\*"({device_id}[\w\.\-]+)"""
"""(?i)deviceDetail(_string)?\\*":"?\{[^\}]*"browser\\*":\\*"({browser}[^\\"]+)"""
"""(?i)deviceDetail(_string)?\\*":"?\{[^\}]*"operatingSystem\\*":\\*"({os}[^\\"]+)"""
""""resourceId":\s*"({resource}[^"]+)""""
""""(app|resource)DisplayName":"({resource}[^"]+)""""
""""resultType":\s*"({error_code}\d+)""""
""""countryOrRegion\\*":\\*"({country_code}[^\\"]+)\\*""""
""""authenticationMethod\\*":\\*"({auth_method}[^\\"]+)\\*""""
""""authenticationProtocol\\*":\\*"(none|({auth_method}[^\\"]+))\\*""""
""""category":\s*"({category}[^"]+)""""
""""riskLevelAggregated":\s*"(none|({severity}[^"]+))""""
"""exa_regex="+time"+:"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}\w+)"+"""
"""exa_regex="TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""
"""exa_regex="TIMEGENERATED=({time}\d{4}-\d{1,2}-\d{1,2}\s\d\d:\d\d:\d\d.\d\d\d)""""
"""exa_regex="TIMEGENERATED":"({time}\d{4}-\d{1,2}-\d{1,2}\s\d\d:\d\d:\d\d(\.\d{1,3})?)""""
"""exa_json_path=$.eventHubsAzureRecord.time,exa_field_name=time""",
"""exa_json_path=$.eventHubsAzureRecord..ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.eventHubsAzureRecord..userPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
"""exa_json_path=$.eventHubsAzureRecord..conditionalAccessStatus,exa_field_name=result""",
"""exa_json_path=$.eventHubsAzureRecord..appDisplayName,exa_field_name=app""",
"""exa_json_path=$.eventHubsAzureRecord.identity,exa_regex=(({user_id}\w+-\w+-\w+-\w+-\w+)|({full_name}({last_name}[^",\s]+)\s*,?\s*({first_name}[^",]+)))""",
"""exa_json_path=$.eventHubsAzureRecord..userDisplayName,exa_regex=([a-f\d]+(\-[a-f\d]+){4}|({full_name}[^"]+))""",
"""exa_json_path=$.eventHubsAzureRecord..userId,exa_field_name=user_id""",
"""exa_json_path=$.eventHubsAzureRecord..deviceDetail.browser,exa_field_name=browser""",
"""exa_json_path=$.eventHubsAzureRecord..deviceDetail.operatingSystem,exa_field_name=os""",
"""exa_json_path=$.eventHubsAzureRecord.operationName,exa_field_name=operation""",
"""exa_json_path=$.eventHubsAzureRecord.identity,exa_regex=({last_name}[^",]+),\s*({first_name}[^",\/]+)(\/[^"]*)?("|$)""",
"""exa_json_path=$.eventHubsAzureRecord..location.countryOrRegion,exa_field_name=country_code"""
"""exa_json_path=$.eventHubsAzureRecord.category,exa_field_name=category"""
"""exa_json_path=$.eventHubsAzureRecord..riskLevelAggregated,exa_field_name=severity,exa_match_expr=!Contains($.eventHubsAzureRecord..riskLevelAggregated,"none")"""
"""exa_json_path=$.time,exa_field_name=time""",
"""exa_json_path=$..ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$..userPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
"""exa_json_path=$..conditionalAccessStatus,exa_field_name=result""",
"""exa_json_path=$..appDisplayName,exa_field_name=app""",
"""exa_json_path=$.identity,exa_regex=(({user_id}\w+-\w+-\w+-\w+-\w+)|({full_name}({last_name}[^",\s]+)\s*,?\s*({first_name}[^",]+)))""",
"""exa_json_path=$..userDisplayName,exa_regex=([a-f\d]+(\-[a-f\d]+){4}|({full_name}[^"]+))""",
"""exa_json_path=$..userId,exa_field_name=user_id""",
"""exa_json_path=$..deviceDetail.browser,exa_field_name=browser""",
"""exa_json_path=$..deviceDetail.operatingSystem,exa_field_name=os""",
"""exa_json_path=$.operationName,exa_field_name=operation""",
"""exa_json_path=$.identity,exa_regex=({last_name}[^",]+),\s*({first_name}[^",\/]+)(\/[^"]*)?("|$)""",
"""exa_json_path=$..location.countryOrRegion,exa_field_name=country_code""",
"""exa_json_path=$.category,exa_field_name=category""",
"""exa_json_path=$..riskLevelAggregated,exa_field_name=severity,exa_match_expr=!Contains($..riskLevelAggregated,"none")""",
"""exa_regex="riskDetail":[^,]+,"({additional_info}[^\]]+),"riskEventTypes"""",
"""exa_regex="location":(\{"geoCoordinates":\{\}\}|({location}\{.*?\}))""",
"""exa_regex=additionalDetails\\*":\s*\\*"({additional_info}[^"\\]+)"""
"""exa_regex=deviceDetail\".+?"deviceId":"[^"]+".+?"displayName":"({src_host}[^"]+)"""",
"""exa_regex=TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)""",
"""exa_regex="resourceId":\s*"({resource}[^"]+)"""",
"""exa_regex="(app|resource)DisplayName":"({resource}[^"]+)"""",
"""exa_json_path=$.properties.resourceId,exa_field_name=resource""",
"""exa_regex="resultType":\s*"({error_code}\d+)"""",
"""exa_regex=UserId"+:"+({user_id}[^"]+)"""
"""exa_regex="(Device)?(b|B)rowser":"({browser}[^"]+)"""
"""exa_regex="UserAgent\\*"+:\\*"+(,|({user_agent}[^"]+))"""
"""exa_regex="(Device)?(o|O)peratingSystem":"({os}[^"]+)"""
"""exa_regex=\\*"(F|f)ailureReason\\*":\\*"({failure_reason}.+?)(\.)?\\*""""
"""exa_regex="ConditionalAccessStatus":"({result}[^"]+)""""
"""exa_regex="IPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""exa_regex="+operationName"+:"+({operation}[^"]+)"+"""
"""exa_regex="+identity"+:"+({last_name}[^",]+),\s*({first_name}[^",\/]+)(\/[^"]*)?""""
"""exa_regex="status":\s*\{[^\}]*?"errorCode":\s*(0|({failure_code}\d+))(,|\})"""
"""exa_regex="AppDisplayName":"\s*({app}[^"]+?)\s*"""",
"""exa_regex="category":\s*"({category}[^"]+)"""",
"""exa_regex="UserPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
"""exa_regex="identity"+:\s*"+(({user_id}\w+-\w+-\w+-\w+-\w+)|({full_name}[^"]+))""""
"""exa_regex=UserDisplayName"+:"+([a-f\d]+(\-[a-f\d]+){4}|({full_name}[^"]+))"""
"""exa_regex="countryOrRegion":"({country_code}[^"]+)""""
""""LocationDetails_string":".+?"city\\":\\"({city}[^\\",]+)\\""""
""""LocationDetails_string":".+?"state\\":\\"({state}[^\\",]+)\\""""
"""exa_regex="LocationDetails_string":".+?"city\\":\\"({city}[^\\",]+)\\""""
"""exa_regex="LocationDetails_string":".+?"state\\":\\"({state}[^\\",]+)\\""""
"""exa_regex=deviceDetail(_string)?\\*":"?\{[^\}]*"displayName\\*":\\*"({src_host}[\w\-\.]+)\$?\s*\\*""",
"""exa_json_path=$..authenticationMethod,exa_field_name=auth_method""",
"""exa_regex="authenticationProtocol\\*":\\*"(none|({auth_method}[^\\"]+))\\*""""
"""exa_json_path=$..servicePrincipalName,exa_field_name=attribute""",
"""exa_json_path=$..servicePrincipalId,exa_field_name=principal_id"""
""""servicePrincipalId":\s*"({principal_id}[^"]+)""""
"""servicePrincipalName":"({attribute}[^",]+)""""
]
DupFields = [ "operation->event_name" ]
ParserVersion = "v1.0.0"


}
```