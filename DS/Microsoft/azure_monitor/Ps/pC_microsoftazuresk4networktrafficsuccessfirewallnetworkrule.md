#### Parser Content
```Java
{
Name = microsoft-azure-sk4-network-traffic-success-firewallnetworkrule
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [""""category":""", """"AzureFirewallNetworkRule"""", """"resourceId":""", """Action: """ ]
  Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""",
    """"resourceId":\s*"({resource_id}[^"]+)"""",
    """"msg":\s*"({additional_info}[^"]+?)\s*"""",
    """"msg":\s*"({protocol}\S+?) request from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?):({src_port}\d{1,5}?) to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?):({dest_port}\d{1,5})""",
    """"operationName":\s*"({operation}[^"]+)"""",
    """"category":\s*"({category}AzureFirewallNetworkRule)""",
    """Action: ({result}(Allow|Deny))""",
    """requestClientApplication=({app}[^=]+?)\s+\w+?=""",
    """Namespace:\s*({event_hub_namespace}[^]]+?)\s*;\s*EventHub name:\s*({event_hub_name}[^]]+?)\]\s*"""
   ]
   ParserVersion = "v1.0.0"


}
```