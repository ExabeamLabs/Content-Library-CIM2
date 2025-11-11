#### Parser Content
```Java
{
Name = microsoft-azure-sk4-network-traffic-success-firewallapp
  Vendor = Microsoft
  Product = Azure Firewall
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [  """"category":""", """"AzureFirewallApplicationRule"""", """"resourceId":""", """Action: Allow""" ]
  Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}(Z|[\+\-]\d\d:\d\d))""",
    """"resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^"]+?))?(\/({resource}[^"\/]+))?)"""",
    """"msg":\s*"({additional_info}[^"]+?)\s*"""",
    """"operationName":\s*"({operation}[^"]+)"""",
    """"msg":\s*"[^"]+?from\s({src_ip}[a-fA-F\d:\.]+?)(:({src_port}\d{1,5}))?\s""",
    """"msg":\s*"[^"]+?to\s(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+))(:({dest_port}\d{1,5}))?\.\s""",
    """Action:\s({action}({result}Allow))""",
    """"msg":\s*"({protocol}[^\s]+)""",
    """requestClientApplication=({app}[^\s]+)""",
    """"({event_name}({category}AzureFirewallApplicationRule))"""",
    """Rule:\s({rule}[^="]+?)(\s\w+=|")""",
    """Policy:\s({policy_name}[^\s]+?)\.\s""",
    """\[Namespace:\s({event_hub_namespace}[^\s;\]]+)\s;\sEventHub name:\s({event_hub_name}[^\]]+)\]"""
  ]


}
```