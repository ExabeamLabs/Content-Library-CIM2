#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-notification-applicationgatewayfirewalllog
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category": "ApplicationGatewayFirewallLog"""",
    """MICROSOFT.NETWORK""",
    """APPLICATIONGATEWAYS"""
  ]
  Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"hostname":\s*"({host}[^"]+)"""",
    """"category":\s*"({category}[^"]+)"""",
    """"operationName":\s*"({operation}[^"]+)"""",
    """"message":\s*"({additional_info}[^"]+)"""",
    """"clientIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"resourceId":\s*"({resource_id}[^"]+)"""",
    """"clientPort":\s*"({src_port}\d+)"""",
    """"action":\s*"({action}[^"]+)"""",
    """"instanceId":\s*"({instance_id}[^"]+)"""",
    """"requestUri":\s*"(({uri_path}[^?"]+)\??({uri_query}[^"]+)?)"""",
    """"ruleSetType":\s*"({rule_type}[^"]+)"""",
    """"ruleId":\s*"({rule_id}[^"]+)"""",
    """"ruleGroup":\s*"({rule}[^"]+)"""",
    """"file":\s*"({file_path}({file_dir}[^\\\/]+[\\\/])({file_name}[^"]+\.({file_ext}[^"]+)))""""
  ]
  DupFields = [ "operation->event_name" ]


}
```