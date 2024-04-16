#### Parser Content
```Java
{
Name = "microsoft-azure-cef-app-login-success-auditlogs"
Vendor = "Microsoft"
Product = "Azure Monitor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
"""ResourceId":"""
"""Category":"AppServiceAuditLogs"""
]
Fields = [
"""\"time\"+:\"+({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}\w+)\""""
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}Z)"""",
"""destinationServiceName =({app}[^\s]+)"""
"""\"Category\":\"({category}[^\"]+)"""
"""suser=(anonymous|\$([\w\-]+)|({user}[\w\.\-]{1,40}\$?))\s+\w+="""
"""\"ResourceId\":\"({object}[^\"]+)\""""
"""\"OperationName\":\"({operation}[^\"]+)"""
"""\"User\":\"(\$([\w\-]+)|({user}[\w\.\-]{1,40}\$?))\""""
"""\"UserDisplayName\":\"({email_address}[^@]+@[^\.]+\.[^\"]+)\""""
"""\"UserAddress\":\"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
"""\"Protocol\":\"({protocol}[^\"]+)\""""
"""\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
]
DupFields = [
"event_hub_namespace->host"
]
ParserVersion = "v1.0.0"


}
```