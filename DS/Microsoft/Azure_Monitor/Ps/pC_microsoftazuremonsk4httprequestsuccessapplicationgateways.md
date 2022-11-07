#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-request-success-applicationgateways
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =Azure""", """"Category":"ApplicationGatewayFirewallLog"""", """"ResourceProvider":"MICROSOFT.NETWORK"""", """"ResourceType":"APPLICATIONGATEWAYS"""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-1.Fields}[
    """"Message":"({additional_info}[^"]+)"""",
    """"clientIP_s":"({src_ip}[A-Fa-f:\d.]+)""""
   ]

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
     """"CallerIpAddress":"({src_ip}[A-Fa-f\d:.]+)"""",
     """"Resource":"({src_host}[^"]+)"""",
     """"TenantId":"({tenant_id}[^"]+)""",
     """"_ResourceId":"({resource_id}[^"]+)"""
   ]
   DupFields = [ "operation->event_name" 
}
```