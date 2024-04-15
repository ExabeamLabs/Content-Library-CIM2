#### Parser Content
```Java
{
Name = "microsoft-azure-cef-app-login-success-authentication"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Azure Monitor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""destinationServiceName =Azure"""
""""operationName":"Authentication""""
"""MICROSOFT.KEYVAULT"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z [\w\-.]+ """
"""\"time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\Wdvc=({host}\S+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\Wact=({operation}[^=]+)\s+(\w+=|$)"""
"""([^\|]*\|){5}({operation}[^\|]+)"""
"""\WflexString1=({operation}[^=]+)\s+(\w+=|$)"""
"""\WdestinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
"""\Wfname=({object}[^=]+)\s+(\w+=|$)"""
"""\Wmsg=({additional_info}[^=]+)\s+(\w+=|$)"""
"""\Wduser=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}.+?))(\s+\w+=|\s*$)"""
"""\Wsuser=(anonymous|({email_address}[^@=]+@[^@=\s]+)|({user}[^\s]+))(\s+|\s*$)"""
"""\Wsuid=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}.+?))(\s+\w+=|\s*$)"""
"""\Woutcome=({result}[^=]+)\s+(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wshost=(|--|({src_host}[^=]+))(\s+\w+=|\s*$)"""
"""\"clientIP\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"description\":\"({additional_info}[^\"]+)"""
"""\"identity\".*?\"claims\".*?\"name\":\"({user}[^\"]+)\""""
"""\"callerIpAddress\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
"""Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]"""
"""EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
"""\[Namespace:\s*({host}\S+) ; EventHub name:"""
"""(?i)({app}Microsoft.KeyVault)"""
"""operationName\":\"({event_name}[^\"]+)\""""
"""resultSignature\":\"({status}[^\"]+)\""""
"""resourceId\":\"({resource}[^\"]+)\""""
"""requestUri\":\"({request_uri}[^\"]+)\""""
"""callerIpAddress\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
"""resultDescription\":\"({additional_info}[^\"]+)\""""
"""claims\/upn\":\"({email_address}[^\"]+)"""
"""\"properties\":.+?\"id\":\"({object}[^\"]+)"""
]
DupFields = ["event_name->operation"]


}
```