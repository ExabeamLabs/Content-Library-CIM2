#### Parser Content
```Java
{
Name = microsoft-azure-cef-network-traffic-rule
   Product = Network Security Group Flow Logs
   ParserVersion = v1.0.0
   Conditions = [
     """"category":"NetworkSecurityGroupRuleCounter""""
   ]
      Fields = ${MicrosoftAzureParsersTemplates.cef-azure-event-hub.Fields}[
    """"operationName":"({operation}[^"]+)""""
] 
}, 

{
    Name = microsoft-azure-json-process-create-success-vmprocess
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Azure Monitor - VM Insights
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      """"Type":"VMProcess"""",
      """ExecutableName"""
    ]
    Fields = [
"""\"TimeGenerated\":\"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
"""Computer\"+:\"+({host}[^\"]+)"""
"""Machine\"+:\"+({src_host}[^\"]+)"""
"""ExecutableName\"+:\"+({process_name}[^\"]+)"""
"""FirstPid\"+:({process_id}\d+)"""
"""\"ExecutablePath\":\"({process_path}((|({process_dir}[^\"]*?))[\\/]+)?({process_name}[^\"\\/]+?))\s*\""""
"""CommandLine\":\"\s*({process_command_line}[^\n]+?)\s*\",\"\w+\""""
"""UserName\"+:\"+((?i)SYSTEM|({user}[\w\.\-]{1,40}\$?))"""
"""UserDomain\"+:\"+({domain}[^\"]+)"""
]
DupFields = [ "process_dir->process_path_directory" ]

cef-azure-event-hub = {
   Vendor = Microsoft
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
   Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z [\w\-.]+ """
     """\"time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
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
     """\"clientIP\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """\"description\":\"({additional_info}[^\"]+)"""
     """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]"""
     """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
     """\[Namespace:\s*({host}\S+) ; EventHub name:"""
     """\"clientIp\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """\"clientPort\":\"({src_port}\d+)"""
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
     """sourceIP\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
     """destinationIP\":\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
     """direction\":\"({direction}[^"]+)"""
     """primaryIPv4Address\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
   
}
```