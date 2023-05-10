#### Parser Content
```Java
{
Name = microsoft-azureatp-json-alert-trigger-success-netlogonbypasssecurityalert
Product = "Azure Advanced Threat Protection"
Conditions = [
  """"category":"""
  """"NetlogonBypassSecurityAlert""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"Azure Advanced Threat Protection""""
]
ParserVersion = "v1.0.0"

defender-atp-events.Fields}[
    """"FileName"+:\s*"+({process_name}[^"]+)""",
    """"FolderPath"+:\s*"+({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-ata-cef-alert-trigger-success-passthehash
Vendor = Microsoft
Product = Microsoft Advanced Threat Analytics
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|PassTheHashSuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[^\s]+))\s+(\w+=|$)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wmsg=[^=]+? used from (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+\w))"""
  """\Wshost=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(\w+=|$)"""
  """\d+:\d+:\d+.+?({dest_ip}\d+\.\d+\.\d+\.\d+).*?CEF:"""
]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-ata-cef-alert-trigger-success-massiveobjectdeletion
Vendor = Microsoft
Product = Microsoft Advanced Threat Analytics
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|MassiveObjectDeletionSuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[^\s]+))\s+(\w+=|$)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wmsg=[^=]+? from domain ({domain}[\w.\-]+\w)"""
  """\Wshost=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(\w+=|$)"""
  """\d+:\d+:\d+.+?({dest_ip}\d+\.\d+\.\d+\.\d+).*?CEF:"""
]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-ata-cef-alert-trigger-success-retrievedata
Vendor = Microsoft
Product = Microsoft Advanced Threat Analytics
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|RetrieveDataProtectionBackupKeySuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[^\s]+))\s+(\w+=|$)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wmsg=[^=]+? from (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+)) .+? ({domain}[\w\.]+) domain .+? from (?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+\w))"""
  """\Wshost=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"
},

${MicrosoftParserTemplates.defender-atp-events}{
  Name = microsoft-defenderep-json-process-create-success-processevents
  Conditions = [  """"Type":"AdvancedHuntingDeviceProcessEvents_CL""", """TimeGenerated""", """TenantId""" ]
  Fields = ${MicrosoftParserTemplates.defender-atp-events.Fields}[
]
ParserVersion = "v1.0.0"
}

{
Name = "microsoft-wapgateway-kv-http-session-thttp"
Vendor = "Microsoft"
Product = "Web Application Proxy-TLS Gateway"
TimeFormat = "yyyy-MM-dd\tHH:mm:ss"
Conditions = [
"""Compression: client="""
"""\thttp\tGET\thttp"""
]
Fields = [
"""(?:-|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)[\s\,]+[\w\s]+[\t\,]+(?:None|Web Proxy)[\t\,]+({web_domain}[^\t\,]+)"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Microsoft"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Fields = [
  """"id":\s*"({alert_id}[^"]+)""""
  """"title":\s*"({alert_name}[^"]+)""""
  """"severity":\s*"({alert_severity}[^"]+)""""
  """"category":\s*"({alert_type}[^"]+)""""
  """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]"""
  """"sourceMaterials":\["({additional_info}[^"]+)"""",
  """"eventDateTime":\s*"({time}[^"]+)""""
  """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))""""
  """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))""""
  """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[^\s"@]+)(@[^"]+)?))""""
  """"userPrincipalName":\s*"({user_upn}[^"]+?)""""
  """"domainName"+:\s*"+(-|({domain}[^"]+))""""
  """"domainName"+:\s*"+(-|({domain}[^"]+))[^}\]]+?userPrincipalName"""
  """"fqdn"+:\s*"+({src_host}[^"]+)""""
  """"+hostStates"+:[^}\]]+?privateIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"+hostStates"+:[^}\]]+?publicIpAddress"+:\s*"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"description":\s*"An actor on\s*({src_host}\S+)\s*performed suspicious"""
  """"fileStates":[^]]+?"name":\s*"({file_name}[^."]+([\.\w]+)?)""""
  """"destinationServiceName":"({app}[^"]+)""""
]
Name = microsoft-azureatp-json-alert-trigger-success-netlogonbypasssecurityalert
Product = "Azure Advanced Threat Protection"
Conditions = [
  """"category":"""
  """"NetlogonBypassSecurityAlert""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"Azure Advanced Threat Protection""""
]
ParserVersion = "v1.0.0"
},

${MicrosoftParserTemplates.defender-atp-security-alert-events}{
  Name = microsoft-azureatp-json-alert-trigger-success-remoteexecutionsecurityalert-1
  Product = Azure Advanced Threat Protection
  ParserVersion = "v1.0.0"
  Conditions = [ """"category":"RemoteExecutionSecurityAlert"""", """vendor":"Microsoft"""", """"sourcetype":"GraphSecurityAlert"""", """provider":"Azure Advanced Threat Protection"""" 
}
```