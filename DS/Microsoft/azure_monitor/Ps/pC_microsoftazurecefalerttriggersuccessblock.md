#### Parser Content
```Java
{
Name = "microsoft-azure-cef-alert-trigger-success-block"
Vendor = "Microsoft"
Product = "Azure Monitor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Conditions = [
  """"category":"FrontdoorWebApplicationFirewallLog""""
  """"action":"Block""""
  """"resourceId":"""
]
Fields = [
  """"time":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""""
  """"host":"({host}[\w\-.]+)"""
  """"clientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"clientPort":"({src_port}\d+)""""
  """"resourceId":"({object}[^"]+)"""
  """"resourceId":"\/([^\/]*\/){7}({dest_host}[\w\-.]+)"""
  """"ruleName":"({policy_name}[^"]+)"""
  """"ruleName":"({alert_name}[^"]+)"""
  """"category":"({alert_type}[^"]+)"""
  """"action":"({action}[^"]+)""""
  """suser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+="""
  """"requestUri":"({url}.+?)",""""
  """Namespace:\s*({host}({event_hub_namespace}\S+))"""
  """EventHub name:\s*({event_hub_name}[^\]\s]+)\s*\]"""
  """"msg":"({alert_name}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```