#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-notification-applicationgateways
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Azure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"SourceSystem":"Azure"""", """"ResourceType":"APPLICATIONGATEWAYS"""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"Message":"({event_name}[^"]+)""",
    """"clientIp_s":"({src_ip}[a-fA-F\d.:]+)""",
    """"hostname_s":"({dest_ip}[a-fA-F\d.:]+)""",
    """"Resource":"({resource}[^"]+)""",
    """"action_s":"({action}[^"]+)""",
    """"ResourceGroup":"({resource_group}[^"]+)""",
# resource_provider is removed
  ]


}
```