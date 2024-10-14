#### Parser Content
```Java
{
Name = microsoft-azure-sk4-network-traffic-success-firewallnetworkrule
  Vendor = Microsoft
  Product = Azure Firewall
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [""""category":""", """"AzureFirewallNetworkRule"""", """"resourceId":""", """Action: """ ]
  Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d(\dZ|[+-]\d\d:\d\d))""",
    """"resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^"]+?))?(\/({resource}[^"\/]+))?)"""",
    """"msg":\s*"({additional_info}[^"]+?)\s*"""",
    """"msg":\s*"({protocol}\S+?) request from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?):({src_port}\d{1,5}?) to ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?):({dest_port}\d{1,5})""",
    """"operationName":\s*"({operation}[^"]+)"""",
    """"category":\s*"({category}AzureFirewallNetworkRule)""",
    """Action: ({result}(Allow|Deny))""",
    """Policy: ({policy_name}[^\s\.]+)""",
    """Rule: ({rule}[^\s\.]+)""",
    """requestClientApplication=({app}[^=]+?)\s+\w+?=""",
    """Namespace:\s*({event_hub_namespace}[^]]+?)\s*;\s*EventHub name:\s*({event_hub_name}[^]]+?)\]\s*"""
   ]
   ParserVersion = "v1.0.0"


}
```