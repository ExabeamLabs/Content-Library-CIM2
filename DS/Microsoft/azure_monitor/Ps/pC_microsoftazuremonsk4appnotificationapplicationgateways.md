#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-notification-applicationgateways
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"SourceSystem":"Azure"""", """"ResourceType":"APPLICATIONGATEWAYS"""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"Message":"({event_name}[^"]+)""",
    """"clientIp_s":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"hostname_s":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"Resource":"({resource}[^"]+)""",
    """"action_s":"({action}[^"]+)""",
    """"ResourceGroup":"({resource_group}[^"]+)""",
# resource_provider is removed
  ]
} 
{
  Name = symantec-endpointprotection-kv-app-notification-eventdescription
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """ SymantecServer: """, """,Event Description: """ ]
  Fields = [
    """(<({alert_severity}({priority}\d+))>)?({time}\w+\s\d+\s\d+:\d+:\d+)?\s*({host}[\w\-.]+)\s+SymantecServer:""",
    """Event time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """Category:\s*({category}[^,]+)""",
    """Event Description:\s*({event_name}[^,]+?)\.?\s*(,|$)"""
  ]


}
```