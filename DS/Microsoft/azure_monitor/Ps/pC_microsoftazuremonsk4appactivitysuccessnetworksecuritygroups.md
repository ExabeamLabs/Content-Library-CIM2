#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-success-networksecuritygroups
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =Azure""", """"Category":"""", """"ResourceProvider":"MICROSOFT.NETWORK"""", """"ResourceType":"NETWORKSECURITYGROUPS"""" ]

azure-ad-activity-1 = {
   Vendor = Microsoft
   Product = Azure Monitor
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Fields = [
     """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
     """"userPrincipalName(\\)?":(\\)?"({email_address}[^"\\]+)""",
     """"OperationName":"({operation}[^"]+)"""",
     """"Result":"({result}[^",]+)"""",
     """"Category":"({category}[^"]+)"""",
     """"UserId":"({user}[^"]+)"""",
     """"CallerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"Resource":"({src_host}[^"]+)"""",
     """"TenantId":"({tenant_id}[^"]+)""",
     """"_ResourceId":"({resource_id}[^"]+)"""
   ]
   DupFields = [ "operation->event_name" 
}
```