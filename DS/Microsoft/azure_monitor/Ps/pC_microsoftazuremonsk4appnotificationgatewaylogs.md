#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-notification-gatewaylogs
  ParserVersion = "v1.0.0"
  Conditions = [ """"_ResourceId"""", """"Category":"GatewayLogs"""", """"Url":"""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-1.Fields}[
    """"Method":"({method}[^"]+)"""",
    """"ResponseCode":({http_response_code}\d+)""",
    """"ClientProtocol":"({protocol}[^"]+)"""",
    """"RequestSize":({bytes_in}\d+)""",
    """"ResponseSize":({bytes_out}\d+)""",
    """"Url":"({url}https?:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)""",
    """Reason":"({failure_reason}[^"]+)"""",
    """Message":"({additional_info}[^"]+)""""
  ]

azure-ad-activity-1 = {
   Vendor = Microsoft
   Product = Azure Monitor
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
   Fields = [
     """"(TimeGenerated|time)":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
     """"userPrincipalName(\\)?":\s*(\\)?"({email_address}[^"\\]+)""",
     """"OperationName":\s*"({operation}[^"]+)"""",
     """"Result":\s*"({result}[^",]+)"""",
     """"Category":\s*"({category}[^"]+)"""",
     """"UserId":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
     """"CallerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"Resource":\s*"({src_host}[^"]+)"""",
     """"TenantId":\s*"({tenant_id}[^"]+)""",
     """"_?ResourceId":\s*"({resource_id}(\/subscriptions\/({subscription_id}[^\/]+))?[^"]*)""""
   ]
   DupFields = [ "operation->event_name" 
}
```