#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-network-session-azurefirewall
  ParserVersion = "v1.0.0"
  Conditions = [ """"ResourceId":""", """"Category":""", """"AzureFirewallNetworkRule"""", """MICROSOFT.NETWORK""", """"OperationName":""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-1.Fields}[
    """"msg(_s)?":\s*"({additional_info}[^"]+?)\s*"""",
    """request from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+) to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)"""
    """Rule Collection:\s*({rule_type}[\w\-]+)"""
    """Rule Collection Group:\s*({rule_source}[\w\-]+)"""
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