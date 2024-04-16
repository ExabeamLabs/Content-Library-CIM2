#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-request-success-applicationgateways
  ParserVersion = "v1.0.0"
  Conditions = [ """"ResourceId":""", """"Category":"ApplicationGatewayFirewallLog"""", """"ResourceProvider":"MICROSOFT.NETWORK"""", """"ResourceType":"APPLICATIONGATEWAYS"""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-1.Fields}[
    """"Message":"({additional_info}[^"]+)"""",
    """"clientIP_s":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
   ]

azure-ad-activity-1 = {
   Vendor = Microsoft
   Product = Azure Monitor
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
   Fields = [
     """"(TimeGenerated|time)":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
     """"userPrincipalName(\\)?":(\\)?"({email_address}[^"\\]+)""",
     """"OperationName":"({operation}[^"]+)"""",
     """"Result":"({result}[^",]+)"""",
     """"Category":"({category}[^"]+)"""",
     """"UserId":"({user}[\w\.\-]{1,40}\$?)"""",
     """"CallerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"Resource":"({src_host}[^"]+)"""",
     """"TenantId":"({tenant_id}[^"]+)""",
     """"_ResourceId":"({resource_id}[^"]+)"""
   ]
   DupFields = [ "operation->event_name" 
}
```