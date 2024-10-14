#### Parser Content
```Java
{
Name = "microsoft-azuread-cef-app-login-clientappused"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd HH:mm:ss.SSS"]
Conditions = [
"""destinationServiceName =Office 365"""
""""isInteractive":"""
""""errorCode":"""
""""clientAppUsed":"""
""""failureReason":"""
"""dproc=Graph Sign-In"""
]
Fields = [
""""createdDateTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d{1,3})"""",
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\w) [\w\-.]+ """
""""createdDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ?)"""
"""\"ipAddress\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F:]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""destinationServiceName\s*=({app}({event_subtype}[^=]+?))\s+(\w+=|$)"""
"""\"appDisplayName\":\"(NotApplicable|({app}[^\"]+?))\s*\""""
"""\WoldFile=({user_agent}[^,]+?)\s+(\w+=|$)"""
"""\"failureReason\":\"({failure_reason}[^\"]+)"""
""""userDisplayName":"\{?(On-Premises Directory Synchronization Service Account|({full_name}({first_name}[^\s"]+?)\s+({last_name}[^"\(\),\-]+)))(\s+[^"]*?"|")"""
"""\"userDisplayName\":\"({full_name}({last_name}[^\",\s]+)\s*,\s*({first_name}[^\",]+?))\s*(\(\w+\))?\""""
"""\"userPrincipalName\":\"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))"""
"""\"userPrincipalName\":\"[^@\s]*?@([\.\w+]+\.)?({email_domain}[^\.\s\"]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))\"""",
""""riskDetail":"({additional_info}[^"]+)""",
"""\sreason=({result_reason}[^=]+?)\s*\w+="""
""""location".+?"city\":\"({location_city}[^\",]+)"""
""""location".+?"state\":\"({location_state}[^\",]+)"""
""""location".+?"countryOrRegion\":\"({country_code}[^\",]+)"""
"""deviceDetail\".+?"displayName\":\"({src_host}[\w\-\.]+)\$?\s*\""""
"""conditionalAccessStatus\":\"(notApplied|({status_msg}[^\",]+))\""""
"""\"clientAppUsed\":\"({object}[^\",]+)"""
"""\"resourceDisplayName\":\"({resource}[^\",]+)"""
"""\"errorCode\":\"*({error_code}\d+)"""
"""\"\"signinErrorCode\":\"*({error_code}\d+)"""
"""userId\":\"({user_id}[^\"]+)"""
"""\"appId\":\"({app_id}[^\"]+)"""
"""\"deviceDetail\".+?"deviceId\":\"({device_id}[^\"]+)"""
"""\"deviceDetail\":\{[^\}]*?\"displayName\":\"({device_name}[^\"]+?)\$?""""
"""\"deviceDetail\":\{[^\}]+?\"operatingSystem\":\"({os}[^\"]+)"""
"""\"deviceDetail\":\{[^\}]+?\"trustType\":\"({trust_type}[^\"]+)"""
"""\"additionalDetails\":\"({additional_info}[^\}\"]+?)\"\}"""
"""CEF:([^\|]*\|){5}({operation}[^\|]+)"""
""""browser":"(|({browser}[^"]+))"""",
""""riskState":"({action}[^"]+)""",
""""correlationId":\s*"({correlation_id}[^"]+)""""
]
DupFields = ["error_code->failure_code"]
ParserVersion = "v1.0.0"


}
```