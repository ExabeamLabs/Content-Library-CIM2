#### Parser Content
```Java
{
Name = microsoft-azuread-sk4-alert-trigger-success-riskyuser
  Product = Azure Monitor
  Vendor = "Microsoft"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""CorrelationId":""", """"Type":"AADRiskyUsers"""", """"OperationName":"Risky user"""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""",
    """destinationServiceName =({app}Azure)""",
    """OperationName":"({operation}[^"]+)""",
    """Category":"({category}[^"]+)""",
    """CallerIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"Type":"({event_category}[^"]+)""",
    """"type":"({additional_info}[^"]+)""",
    """"Resource":"({resource}[^"]+)""",
    """"ResourceId":"({resource_id}[^",]+)""",
    """"UserPrincipalName":"({email_user}[^"@]+@[^"@]+)"""",
    """"UserDisplayName":"(({first_name}[^\s"]+)\s+({last_name}[^\s"]+))"""",
    """"RiskState":"({result}[^"]+)"""
  ]
  DupFields = ["category->event_name","event_category->alert_type"]


}
```