#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-success-containerservice
 Vendor = Microsoft
 Product = Azure Kubernetes Service
 ParserVersion = "v1.0.0"
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
 Conditions = [  """"operationName":""", """"Microsoft.ContainerService""", """"category":""",""""resourceId":""", """"pod":""" ]
 Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({service_name}Microsoft.ContainerService)""",
    """"Microsoft.ContainerService\/({operation}[^"]+)""",
    """"user\\?":\s*\{\\?"username\\?":\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?"""",
    """"sourceIPs\\?":\s*\[\\?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"userAgent\\?":\s*\\?"({user_agent}[^"]+)\\?"""",
    """"operation":\s*"({action}[^"]+)"""",
    """"roleDefinitionId":\s*"({role}[^"]+)""",
    """"resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^"]+?))?(\/({resource}[^"\/]+))?)"""",
    """\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)""",
    """"operationName":\s*"({operation}[^"]+)"""",
    """"category":\s*"({category}[^"]+)"""",
    """"containerID":\s*"({container_id}[^"]+)"""",
    """"name\\?":\\?"({object}[^"]+?)\\"""",
 ]


}
```