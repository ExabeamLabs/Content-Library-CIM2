#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-success-containerservice
 Vendor = Microsoft
 Product = Azure Monitor
 ParserVersion = "v1.0.0"
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
 Conditions = [ """destinationServiceName =Azure""", """"operationName":"Microsoft.ContainerService""", """"category":"kube-audit-admin"""" ]
 Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({service_name}Microsoft.ContainerService)""",
    """"Microsoft.ContainerService\/({operation}[^"]+)""",
    """"user":\{"username":"({user}[^"]+)"""",
    """"sourceIPs":\["({src_ip}[^"]+)""",
    """"userAgent":"({user_agent}[^"]+)""",
    """"operation":"({action}[^"]+)"""",
    """"roleDefinitionId":"({role}[^"]+)""",
    """"resourceId":".*\/RESOURCEGROUPS\/({account_id}[^\/]+)""", 
    """\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
 ]
 DupFields= ["event_hub_namespace->host"]


}
```