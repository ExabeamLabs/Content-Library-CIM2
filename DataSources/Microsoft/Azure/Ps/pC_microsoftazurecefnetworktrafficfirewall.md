#### Parser Content
```Java
{
Name = microsoft-azure-cef-network-traffic-firewall
   ParserVersion = v1.0.0
   Conditions = [
     """"category":"ApplicationGatewayFirewallLog"""",
     """destinationServiceName =Azure"""
   ]
   Fields = ${MicrosoftAzureParsersTemplates.cef-azure-event-hub.Fields}[
    """"operationName":"({operation}[^"]+)""""
] 

cef-azure-event-hub = {
   Vendor = Microsoft
   Product = Azure
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
   Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z [\w\-.]+ """
     """\"time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
     """\Wdvc=({host}\S+)"""
     """\Wdvchost=({host}[\w\-.]+)"""
     """\Wact=({operation}[^=]+)\s+(\w+=|$)"""
     """([^\|]*\|){5}({operation}[^\|]+)"""
     """\WflexString1=({operation}[^=]+)\s+(\w+=|$)"""
     """\WdestinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
     """\Wfname=({object}[^=]+)\s+(\w+=|$)"""
     """\Wmsg=({additional_info}[^=]+)\s+(\w+=|$)"""
     """\Wduser=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}.+?))(\s+\w+=|\s*$)"""
     """\Wsuser=(anonymous|({email_address}[^@=]+@[^@=\s]+)|({user}[^\s]+))(\s+|\s*$)"""
     """\Wsuid=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}.+?))(\s+\w+=|\s*$)"""
     """\Woutcome=({result}[^=]+)\s+(\w+=|$)"""
     """\Wsrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
     """\Wshost=(|--|({src_host}[^=]+))(\s+\w+=|\s*$)"""
     """\"clientIP\":\"({src_ip}[A-Fa-f.\d]+)"""
     """\"description\":\"({additional_info}[^\"]+)"""
     """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]"""
     """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
     """\[Namespace:\s*({host}\S+) ; EventHub name:"""
     """\"clientIp\":\"({src_ip}[^\"]+)"""
     """\"clientPort\":\"({src_port}\d+)"""
     """\"requestUri\":\"({request_uri}[^\"]+)"""
     """\"ruleSetType\":\"({rule}[^\"]+)"""
     """\"ruleId\":\"({rule_id}[^\"]+)"""
     """\"ruleGroup.+?\"message\":\"({additional_info}[^\"]+)"""
     """\"action\":\"({action}[^\"]+)"""
     """\"transactionId\":\"({transaction_id}[^\"]+)"""
     """\"file\":\"({file_path}({file_dir}[^\/\"]+)\/({file_name}[^\"]+))"""
     """\WrequestClientApplication=(|({app}.+?))(\s+\w+=|\s*$)"""
     """originalHost":"(({src_ip}[A-Fa-f\d.:]+)|({src_host}.+?[^\\]))""""
     """category\":\"({operation}[^"]+)"""
     """type\":\"({action}[^"]+)"""
     """ruleName\":\"({rule}[^"]+)"""
     """sourceIP\":\"({src_ip}[^"]+)"""
     """destinationIP\":\"({dest_ip}[^"]+)"""
     """direction\":\"({direction}[^"]+)"""
     """primaryIPv4Address\":\"({src_ip}[^"]+)"""
   
}
```