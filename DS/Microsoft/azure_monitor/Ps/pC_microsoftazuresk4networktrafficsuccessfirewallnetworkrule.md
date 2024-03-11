#### Parser Content
```Java
{
Name = microsoft-azure-sk4-network-traffic-success-firewallnetworkrule
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """destinationServiceName =Azure""", """"category":"AzureFirewallNetworkRule"""", """"resourceId":"""", """dproc=EventHub""", """Action: Allow""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""",
    """"resourceId":"({resource_id}[^"]+)"""",
    """"msg":"({additional_info}[^"]+?)\s*"""",
    """"msg":"({protocol}\S+?) request from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?):({src_port}\d{1,5}?) to ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?):({dest_port}\d{1,5})""",
    """"operationName":"({operation}[^"]+)"""",
    """"category":"({category}AzureFirewallNetworkRule)""",
    """Action: ({action}Allow)""",
    """requestClientApplication=({app}[^=]+?)\s+\w+?=""",
    """Namespace:\s*({event_hub_namespace}[^]]+?)\s*;\s*EventHub name:\s*({event_hub_name}[^]]+?)\]\s*"""
   ]
   ParserVersion = "v1.0.0"


}
```