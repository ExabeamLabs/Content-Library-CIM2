#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-applicationgatewayaccess
  ParserVersion = "v1.0.0"
  Conditions = [ """ResourceId":""", """"Category":"ApplicationGatewayAccessLog"""", """"OperationName":"ApplicationGatewayAccess"""", """"ResourceProvider":"MICROSOFT.NETWORK"""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-1.Fields}[
    """"httpMethod_s":"({method}[^"]+)"""",
    """"requestUri_s":"({uri}[^"]+)"""",
    """"clientIP_s":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"clientPort_d":({src_port}\d+)""",
    """"httpStatus_d":({result_code}\d+)""",
    """"receivedBytes_d":({bytes_out}\d+)""",
    """"sentBytes_d":({bytes_in}\d+)""",
    """"serverRouted_s":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)"""
    """"ResourceId":"({object}[^",]+)"""
    """"userAgent_s"+:"+({user_agent}[^"]+)?"+,"""
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
     """"CallerIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"Resource":\s*"({src_host}[^"]+)"""",
     """"TenantId":\s*"({tenant_id}[^"]+)""",
     """"(_)?ResourceId":\s*"({resource_id}[^"]+)"""
   ]
   DupFields = [ "operation->event_name" 
}
```