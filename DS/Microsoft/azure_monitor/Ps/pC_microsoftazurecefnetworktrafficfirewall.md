#### Parser Content
```Java
{
Name = microsoft-azure-cef-network-traffic-firewall
   Product = Azure Monitor
   ParserVersion = v1.0.0
   Vendor = Microsoft
   TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss" , "yyyy-MM-dd'T'HH:mm:ssZ" ]
   Conditions = [""""category":"ApplicationGatewayFirewallLog"""",""""resourceId":""" ]
   Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z [\w\-.]+ """
     """\"time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d:\d+)"""
     """\Wdvc=({host}\S+)"""
     """\Wdvchost=({host}[\w\-.]+)"""
     """\Wact=({operation}[^=]+)\s+(\w+=|$)"""
     """\WflexString1=({operation}[^=]+)\s+(\w+=|$)"""
     """\Wfname=({object}[^=]+)\s+(\w+=|$)"""
     """\Wmsg=({additional_info}[^=]+)\s+(\w+=|$)"""
     """\Wduser=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)"""
     """\Wsuser=(anonymous|({email_address}[^@=]+@[^@=\s]+)|({user}[\w\.\-]{1,40}\$?))(\s+|\s*$)"""
     """\Wsuid=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)"""
     """\Woutcome=({result}[^=]+)\s+(\w+=|$)"""
     """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """\Wshost=(|--|({src_host}[^=]+))(\s+\w+=|\s*$)"""
     """\"description\":\"({additional_info}[^\"]+)"""
     """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]"""
     """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
     """\[Namespace:\s*({host}\S+) ; EventHub name:"""
     """"properties":\s*\{.+?\"(?i)clientIp\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """"properties":\s*\{.+?\"clientPort\":\"({src_port}\d+)"""
     """\"requestUri\":\"({uri}[^\"]+)"""
     """\"ruleSetType\":\"({rule}[^\"]+)"""
     """\"ruleId\":\"({rule_id}[^\"]+)"""
     """\"ruleGroup.+?\"message\":\"({additional_info}[^\"]+)"""
     """\"transactionId\":\"({transaction_id}[^\"]+)"""
     """\"file\":\"({file_path}({file_dir}[^\/\"]+)\/({file_name}[^\"]+))"""
     """\WrequestClientApplication=(|({app}.+?))(\s+\w+=|\s*$)"""
     """destinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
     """originalHost":"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?[^\\]))""""
     """category\":\"({operation}[^"]+)"""
     """type\":\"({action}[^"]+)"""
     """\"action\":\"({action}[^\"]+)"""
     """ruleName\":\"({rule}[^"]+)"""
     """direction\":\"({direction}[^"]+)"""
     """"operationName":"({operation}[^"]+)"""" 
     """"category":"({category}[^"]+)""""
     """"instanceId":\s*"({instance_id}[^"]+)""""
     """"hostname":"({host}[\w\-\.]+)""""
     """"requestUri":"({uri}[^"]+)""""
     """"resourceId":"({object}[^",]+)""""
     """"resourceId":\s*"({resource_id}(\/SUBSCRIPTIONS\/({subscription_id}[^\/]+))?(\/RESOURCEGROUPS\/({resource_group}[^\/]+))?(\/PROVIDERS\/({provider_name}[^\/]+))?\/[^"]+)""""
     """RemoteAddr, with value ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
   ]


}
```