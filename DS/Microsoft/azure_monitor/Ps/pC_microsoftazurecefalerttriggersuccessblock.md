#### Parser Content
```Java
{
Name = "microsoft-azure-cef-alert-trigger-success-block"
Vendor = "Microsoft"
Product = "Azure Monitor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
  """destinationServiceName =Azure"""
  """"category":"FrontdoorWebApplicationFirewallLog""""
  """"action":"Block""""
]
Fields = [
  """"time":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""""
  """"host":"({host}[^"]+)"""
  """"clientIP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"clientPort":"({src_port}\d+)""""
  """"resourceId":"({object}[^"]+)"""
  """"resourceId":"\/([^\/]*\/){7}({dest_host}[^"]+)"""
  """"ruleName":"({policy_name}[^"]+)"""
  """"ruleName":"({alert_name}[^"]+)"""
  """"category":"({alert_type}[^"]+)"""
  """"action":"({action}[^"]+)""""
  """suser=(anonymous|({user}[^=]+?))\s+\w+="""
  """"requestUri":"({url}.+?)",""""
  """Namespace:\s*({event_hub_namespace}\S+)"""
  """EventHub name:\s*({event_hub_name}[^\]\s]+)\s*\]"""
  """"msg":"({alert_name}[^"]+)""""
]
DupFields = [
  "event_hub_namespace->host"
]
ParserVersion = "v1.0.0"


}
```