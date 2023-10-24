#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-destinationservicename
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [""""category":"ContainerRegistryRepositoryEvents"""", """"operationName""""]
  Fields = [
    """"loginServer":"({host}[^",]+)""",
    """"time":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+Z)""",
    """({app}ContainerRegistry)""",
    """({event_name}ContainerRegistryRepositoryEvents)""",
    """"identity":"(({email_address}[^@,]+@[^",]+)|({user}[\w\.\-]{1,40}\$?))""",
    """"resultDescription":"({result_code}\d+)""",
    """"callerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"userAgent":"({user_agent}[^"]+)"""",
    """"operationName":"({operation}[^",]+)""",
# repository is removed
    """"resourceId":"({resource}[^",]+)""",
    """"tag":"({tag}[^",]+)""",
# digest is removed
    """"mediaType":"({mime}[^",]+)""",
    """"location":"({region}[^",]+)""",
    """"tenantId":"({tenant_id}[^",]+)""",
    """"durationMs":"({duration}[^",]+)""",
# artifact_type is removed
    """"correlationId":"({correlation_id}[^",]+)""",
    """({category}ContainerRegistryRepositoryEvents)""",
    """\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)""",
    """"userAgent":".+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin|Ubuntu)"""
  ]
  DupFields = [ "repository->object", "event_hub_namespace->host" ]
  ParserVersion = "v1.0.0"


}
```