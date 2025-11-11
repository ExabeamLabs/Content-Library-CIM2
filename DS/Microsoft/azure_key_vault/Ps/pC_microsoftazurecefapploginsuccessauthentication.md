#### Parser Content
```Java
{
Name = "microsoft-azure-cef-app-login-success-authentication"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Azure Key Vault"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSS" ]
Conditions = [
""""resourceId":"""
""""operationName":"Authentication""""
"""MICROSOFT.KEYVAULT"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z [\w\-.]+ """
"""\"(time|TimeGenerated)\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?)"""
"""\Wdvc=({host}\S+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wact=({operation}[^=]+)\s+(\w+=|$)"""
"""([^\|]*\|){5}({operation}[^\|]+)"""
"""\WflexString1=({operation}[^=]+)\s+(\w+=|$)"""
"""destinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
"""\Wfname=({object}[^=]+)\s+(\w+=|$)"""
"""\Wmsg=({additional_info}[^=]+)\s+(\w+=|$)"""
"""\Wduser=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""\Wsuser=(anonymous|({email_address}[^@=]+@[^@=\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+|\s*$)"""
"""\Wsuid=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""\Woutcome=({result}[^=]+)\s+(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wshost=(|--|({src_host}[^=]+))(\s+\w+=|\s*$)"""
"""\"clientIP\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"description\":\"({additional_info}[^\"]+)"""
"""\"identity\".*?\"claims\".*?\"name\":\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
"""\"callerIpAddress\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
"""Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]"""
"""EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
"""\[Namespace:\s*({host}\S+) ; EventHub name:"""
"""(?i)({app}Microsoft.KeyVault)"""
"""operationName\":\"({operation}({event_name}[^\"]+))\""""
"""resultSignature\":\"({status_msg}[^\"]+)\""""
"""resourceId\":\"({resource_id}\/SUBSCRIPTIONS\/({subscription_id}[^\/]+)\/RESOURCEGROUPS\/({resource_group}[^\/]+)(\/PROVIDERS\/({provider_name}[^\/]+))?(\/[^\/"]*)\/({resource}[^\"]+))\""""
"""requestUri\":\"({uri}[^\"]+)\""""
"""callerIpAddress\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
"""resultDescription\":\"({additional_info}[^\"]+)\""""
"""claims\/upn\":\"({email_address}[^\"]+)"""
"""\"properties\":.+?\"id\":\"({object}[^\"]+)"""
]


}
```