#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-network-session-azurefirewall
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =Azure""", """"Category":"AzureFirewallNetworkRule"""", """"ResourceProvider":"MICROSOFT.NETWORK"""", """"ResourceType":"AZUREFIREWALLS"""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-1.Fields}[
    """"msg_s":"({additional_info}[^"]+?)\s*"""",
    """request from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+) to ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)"""
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
     """"CallerIpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"Resource":"({src_host}[^"]+)"""",
     """"TenantId":"({tenant_id}[^"]+)""",
     """"_ResourceId":"({resource_id}[^"]+)"""
   ]
   DupFields = [ "operation->event_name" 
}
```