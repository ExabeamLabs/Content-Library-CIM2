#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-success-containerservice
 Vendor = Microsoft
 Product = Azure Monitor
 ParserVersion = "v1.0.0"
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
 Conditions = [  """"operationName":""", """"Microsoft.ContainerService""", """"category":""",""""resourceId":""", """"pod":""" ]
 Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({service_name}Microsoft.ContainerService)""",
    """"Microsoft.ContainerService\/({operation}[^"]+)""",
    """"user":\s*\{"username":"({user}[\w\.\-]{1,40}\$?)"""",
    """"sourceIPs":\s*\["({src_ip}[^"]+)""",
    """"userAgent":\s*"({user_agent}[^"]+)""",
    """"operation":\s*"({action}[^"]+)"""",
    """"roleDefinitionId":\s*"({role}[^"]+)""",
    """"resourceId":\s*".*\/RESOURCEGROUPS\/({account_id}[^\/]+)""",
    """\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
 ]
 DupFields= ["event_hub_namespace->host"]


}
```