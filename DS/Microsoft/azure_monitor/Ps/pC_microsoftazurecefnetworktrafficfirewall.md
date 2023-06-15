#### Parser Content
```Java
{
Name = microsoft-azure-cef-network-traffic-firewall
   Product = Azure Monitor
   ParserVersion = v1.0.0
   Vendor = Microsoft
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
   Conditions = [
     """"category":"ApplicationGatewayFirewallLog"""",
     """destinationServiceName =Azure"""
   ]
   Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z [\w\-.]+ """
     """\"time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
     """\Wdvc=({host}\S+)"""
     """\Wdvchost=({host}[\w\-.]+)"""
     """\Wact=({operation}[^=]+)\s+(\w+=|$)"""
     """\WflexString1=({operation}[^=]+)\s+(\w+=|$)"""
     """\Wfname=({object}[^=]+)\s+(\w+=|$)"""
     """\Wmsg=({additional_info}[^=]+)\s+(\w+=|$)"""
     """\Wduser=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}.+?))(\s+\w+=|\s*$)"""
     """\Wsuser=(anonymous|({email_address}[^@=]+@[^@=\s]+)|({user}[^\s]+))(\s+|\s*$)"""
     """\Wsuid=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}.+?))(\s+\w+=|\s*$)"""
     """\Woutcome=({result}[^=]+)\s+(\w+=|$)"""
     """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """\Wshost=(|--|({src_host}[^=]+))(\s+\w+=|\s*$)"""
     """\"clientIP\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """\"description\":\"({additional_info}[^\"]+)"""
     """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]"""
     """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
     """\[Namespace:\s*({host}\S+) ; EventHub name:"""
     """\"clientIp\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """\"clientPort\":\"({src_port}\d+)"""
     """\"requestUri\":\"({request_uri}[^\"]+)"""
     """\"ruleSetType\":\"({rule}[^\"]+)"""
     """\"ruleId\":\"({rule_id}[^\"]+)"""
     """\"ruleGroup.+?\"message\":\"({additional_info}[^\"]+)"""
     """\"action\":\"({action}[^\"]+)"""
     """\"transactionId\":\"({transaction_id}[^\"]+)"""
     """\"file\":\"({file_path}({file_dir}[^\/\"]+)\/({file_name}[^\"]+))"""
     """\WrequestClientApplication=(|({app}.+?))(\s+\w+=|\s*$)"""
     """\WdestinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
     """originalHost":"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?[^\\]))""""
     """category\":\"({operation}[^"]+)"""
     """type\":\"({action}[^"]+)"""
     """ruleName\":\"({rule}[^"]+)"""
     """direction\":\"({direction}[^"]+)"""
     """"operationName":"({operation}[^"]+)"""" 
   ]


}
```