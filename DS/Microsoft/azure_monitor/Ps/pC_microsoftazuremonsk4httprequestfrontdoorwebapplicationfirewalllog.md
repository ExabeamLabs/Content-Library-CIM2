#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-request-frontdoorwebapplicationfirewalllog
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"FrontdoorWebApplicationFirewallLog"""",
    """"action":"Allow""""
  ]
  Fields = [
    """"time":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""",
    """"host":"({host}[^"]+)""",
    """"clientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"clientPort":"({src_port}\d+)""""
    """"resourceId":"({object}[^"]+)"""
    """"resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""""
    """"resourceId":"\/([^\/]*\/){7}({dest_host}[\w\-.]+)""",
    """"ruleName":"({alert_name}[^"]+)""",
    """"category":"({alert_type}[^"]+)""",
    """"action":"({action}[^"]+)""""
    """suser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=""",
    """"requestUri":"({url}[^"]+)"""",
    """Namespace:\s*({event_hub_namespace}\S+)""",
    """EventHub name:\s*({event_hub_name}[^\]\s]+)\s*\]""",
    """"operationName":"({operation}[^"]+)""",
    """destinationServiceName =({app}[^=]+)\s+(\w+=|$)""",
    """category":"({category}[^"]+)""""
# policy_mode is removed
  ]
   DupFields= ["event_hub_namespace->host", "object->resource" ]


}
```