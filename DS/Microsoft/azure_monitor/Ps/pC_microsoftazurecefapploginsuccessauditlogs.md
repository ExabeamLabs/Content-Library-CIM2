#### Parser Content
```Java
{
Name = "microsoft-azure-cef-app-login-success-auditlogs"
Vendor = "Microsoft"
Product = "Azure Monitor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [ """ResourceId":""", """Category":""", """"AppService""", """AuditLogs""", """"OperationName":""", """"Authorization"""" ]
Fields = [
"""\"time\"+:\s*\"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}\w+)\""""
""""TimeGenerated":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}Z)"""",
"""destinationServiceName =({app}[^\s]+)"""
"""\"Category\":\s*\"({category}[^\"]+)"""
"""suser=(anonymous|\$([\w\-]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+="""
"""\"ResourceId\":\s*\"({object}[^\"]+)\""""
"""\"OperationName\":\s*\"({operation}[^\"]+)"""
"""\"User\":\s*\"(\$([\w\-]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\""""
"""\"UserDisplayName\":\s*\"({email_address}[^@]+@[^\.]+\.[^\"]+)\""""
"""\"UserAddress\":\s*\"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
"""\"Protocol\":\s*\"({protocol}[^\"]+)\""""
"""\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
""""Result":\s*"({result}[^"]+)""""
""""CsHost":\s*"({host}[\w\-.]+)""""
""""Details":\s*"({additional_info}[^"]+)""""
]
DupFields = [
"event_hub_namespace->host"
]
ParserVersion = "v1.0.0"


}
```