#### Parser Content
```Java
{
Name = "microsoft-o365-cef-app-login-appdisplayname"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """destinationServiceName =Office 365""", """"appDisplayName":""", """"failureReason":""", """dproc""" ]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\w) [\w\-.]+ """
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsuser=(\w+-\w+-\w+-\w+-\w+|Sync|System|NotApplicable|({email_address}[^@\s]+?@[^@\s]+?)|({user}[^@\s]+?))\s+(\w+=|$)"""
"""\Wsuser=[^@\s]*?@([\.\w+]+\.)?({email_domain}[^\.\s]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))\s+"""
"""\Wrequest=({result}[^=]+?)\s+(\w+=|$)"""
"""CEF:([^\|]*\|){5}({operation}[^\|]+)""",
"""\WflexString1=({operation}[^=]+?)\s+(\w+=|$)"""
"""\WdestinationServiceName\s*=({app}({event_subtype}[^=]+?))\s+(\w+=|$)"""
""""appDisplayName":"({app}[^"]+?)\s*"""",
"""\WsourceServiceName =({app}[^=]+?)\s+(\w+=|$)"""
"""\WoldFile=({user_agent}[^,]+?)\s+(\w+=|$)"""
"""\"failureReason\":\"({failure_reason}[^\"]+)"""
""""userDisplayName":"({full_name}[^"]+)""",
""""userId":"({user_sid}[^"]+)""",
"""\"userDisplayName\":\"({full_name}({first_name}[^\s\"]+?)\s+({last_name}[^\s\"\(\),]+))\s*[^\"]*?\""""
"""\"userDisplayName\":\"({full_name}({last_name}[^\",\s]+)\s*,\s*({first_name}[^\",]+?))\s*(\(\w+\))?\""""
"""\"userPrincipalName\":\"({email_address}[^\"\s@]+@[^\"\s@]+)"""
"""\"userPrincipalName\":\"[^@\s]*?@([\.\w+]+\.)?({email_domain}[^\.\s\"]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))\""""
"""\sreason=({additional_info}[^=]+?)\s*\w+="""
"""city\":\"({location_city}[^\",]+)"""
"""state\":\"({location_state}[^\",]+)"""
"""countryOrRegion\":\"({country_code}[^\",]+)"""
"""\"browser\":\"({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident|IE|Edge)"""
"""\"operatingSystem\":\"({os}[^\",]+)\""""
"""deviceDetail\":\{[^\}]+?displayName\":\"({src_host}[^\",]+)\""""
"""conditionalAccessStatus\":\"({status}[^\",]+)\""""
"""\"clientAppUsed\":\"({object}[^\",]+)"""
"""\"resourceDisplayName\":\"({resource}[^\",]+)"""
"""\"errorCode\":({error_code}\d+)"""
"""\"signinErrorCode\":({error_code}\d+)"""
""""deviceInformation":"(\;{1,5}|\;?({additional_info}[^"]+))""""
"""country(OrRegion)?":"({country_code}[^",]+)"""
]
ParserVersion = "v1.0.0"


}
```