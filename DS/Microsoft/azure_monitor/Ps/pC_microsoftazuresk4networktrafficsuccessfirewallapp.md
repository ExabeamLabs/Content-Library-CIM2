#### Parser Content
```Java
{
Name = microsoft-azure-sk4-network-traffic-success-firewallapp
  Vendor = Microsoft
  Product = Azure Monitor
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [  """"category":"AzureFirewallApplicationRule"""", """"resourceId":"""", """Action: Allow""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""",
    """"resourceId":"({resource_id}[^"]+)"""",
    """"msg":"({additional_info}[^"]+?)\s*"""",
    """"operationName":"({operation}[^"]+)"""",
    """"msg":"[^"]+?from\s({src_ip}[a-fA-F\d:\.]+?)(:({src_port}\d{1,5}))?\s""",
    """"msg":"[^"]+?to\s(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+))(:({dest_port}\d{1,5}))?\.\s""",
    """Action:\s({result}Allow)""",
    """"msg":"({protocol}[^\s]+)""",
    """requestClientApplication=({app}[^\s]+)""",
    """"({category}AzureFirewallApplicationRule)"""",
    """Rule:\s({rule}[^=]+?)\s\w+=""",
    """Policy:\s({policy_name}[^\s]+?)\.\s""",
    """\[Namespace:\s({event_hub_namespace}[^\s;\]]+)\s;\sEventHub name:\s({event_hub_name}[^\]]+)\]"""
  ]
  DupFields = [ "category->event_name", "result->action" ]


}
```