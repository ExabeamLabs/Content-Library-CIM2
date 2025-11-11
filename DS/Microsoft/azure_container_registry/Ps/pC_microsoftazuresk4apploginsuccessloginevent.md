#### Parser Content
```Java
{
Name = "microsoft-azure-sk4-app-login-success-loginevent"
Vendor = "Microsoft"
Product = "Azure Container Registry"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
""""category":"ContainerRegistryLoginEvents""""
""""operationName":"Login""""
]
Fields = [
""""loginServer":"({host}[^",]+)"""
""""time":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+Z)"""
"""({app}ContainerRegistry)"""
"""({event_name}ContainerRegistryLoginEvents)"""
""""identity":"(({email_address}[^@,]+@[^",]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
""""resultDescription":"({result_code}\d+)"""
""""callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""userAgent":"({user_agent}[^"]+)""""
""""operationName":"({operation}[^",]+)"""
"""\[Namespace:\s*({host}({event_hub_namespace}\S+)) ; EventHub name:\s*({event_hub_name}[\w-]+)"""
""""loginServer":"({auth_server}[^"]+)""""
""""({category}ContainerRegistryLoginEvents)""""
""""resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^"]+?))?(\/({resource}[^"\/]+))?)""""
""""location":"({region}[^",]+)"""
""""tenantId":"({tenant_id}[^",]+)"""
""""durationMs":"({duration}[^",]+)"""
""""correlationId":"({correlation_id}[^",]+)"""
]
ParserVersion = "v1.0.0"


}
```