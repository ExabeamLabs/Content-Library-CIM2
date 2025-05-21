#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-azurefrontdoor
  Product = Azure Monitor
  Vendor = "Microsoft"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions=[
    """"ActionType":"""
    """CloudAppEvents""""
  ]
  Fields = [
	"""EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
    """\[Namespace:\s*({host}\S+) ; EventHub name:"""
    """"operationName":"({operation}[^"]+)""""
    """"category":"({category}[^"]+)""""
    """"(time|TimeGenerated)":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)"""
    """"IPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
    """"resourceProvider":"({service_name}[^"]+)"""
    """"ActivityObjects":\[.+?"Type":"Resource","Id":"({resource}({resource_path}[^"]+)\/({resource_name}[^"]+)|[^"]+)""""
    """"Application":"({app}[^"]+)"""
    """"Tenant":"DefaultTenant","tenantId":"({tenant_id}[^"]+)"""
    """"Role":"Actor","Type":"User".+?"AccountDisplayName":"({full_name}({first_name}[^\s\"]+)\s({last_name}[^\s\"\(]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```