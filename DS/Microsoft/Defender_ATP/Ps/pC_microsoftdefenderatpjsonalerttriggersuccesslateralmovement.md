#### Parser Content
```Java
{
Name = microsoft-defenderatp-json-alert-trigger-success-lateralmovement
Product = Defender ATP
Conditions = [
  """"category":"""
  """"LateralMovement""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"Microsoft Defender ATP""""
]
ParserVersion = "v1.0.0"

cef-defender-atp-2.Fields} [
     """ProcessId":({process_id}\d+)""",
     """InitiatingProcessFileName":\s*"({parent_process}[^"]+)""",
     """"FileName":\s*"({process_name}[^"]+)""",
     """DeviceName":\s*"({dest_host}[^"]+)""",
     """ProcessCommandLine":\s*"({process_command_line}[^"]+)\s*""""
     """MD5":"({hash_md5}[^"]+)""",
 ]
 ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Azure Advanced Threat Protection
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
  """CEF:?([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wshost=(({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({src_host}[\w\-.]+))"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wcs1=({malware_url}.+?)\s+(\w+=|$).+?cs1Label=url"""
  """\Wcs1Label=url.*?\Wcs1=({malware_url}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^\s]+)\s"""
  """\Wcs2=({result}[^\s]+)"""
]
Name = microsoft-azureatp-cef-alert-trigger-success-securityalert
Conditions = [
  """CEF"""
  """|Microsoft|Azure ATP|"""
  """|SamrReconnaissanceSecurityAlert|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Azure Advanced Threat Protection
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
  """CEF:?([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wshost=(({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({src_host}[\w\-.]+))"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wcs1=({malware_url}.+?)\s+(\w+=|$).+?cs1Label=url"""
  """\Wcs1Label=url.*?\Wcs1=({malware_url}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[^\s]+)\s"""
  """\Wcs2=({result}[^\s]+)"""
]
Name = microsoft-azureatp-cef-alert-trigger-success-enumerationsecurityalert
Conditions = [
  """CEF"""
  """|Microsoft|Azure ATP|"""
  """|AccountEnumerationSecurityAlert|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Fields = [
  """"id":\s*"({alert_id}[^"]+)""""
  """"title":\s*"({alert_name}[^"]+)""""
  """"severity":\s*"({alert_severity}[^"]+)""""
  """"category":\s*"({alert_type}[^"]+)""""
  """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]"""
  """"eventDateTime":\s*"({time}[^"]+)""""
  """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))""""
  """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))""""
  """"logonIp":\s*"({src_ip}[a-fA-F:\d.]+)""""
  """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[^\s"@]+)(@[^"]+)?))""""
  """"userPrincipalName":\s*"({user_upn}[^"]+?)""""
  """"domainName"+:\s*"+(-|({domain}[^"]+))""""
  """"domainName"+:\s*"+(-|({domain}[^"]+))[^}\]]+?userPrincipalName"""
  """"fqdn"+:\s*"+({src_host}[^"]+)""""
  """"+hostStates"+:[^}\]]+?privateIpAddress"+:\s*"+({src_ip}[a-fA-F:\d.]+)"""
  """"+hostStates"+:[^}\]]+?publicIpAddress"+:\s*"+({dest_ip}[a-fA-F:\d.]+)"""
  """"description":\s*"An actor on\s*({src_host}\S+)\s*performed suspicious"""
  """"fileStates":[^]]+?"name":\s*"({file_name}[^."]+([\.\w]+)?)""""
]
Name = microsoft-defenderatp-json-alert-trigger-success-lateralmovement
Product = Defender ATP
Conditions = [
  """"category":"""
  """"LateralMovement""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"Microsoft Defender ATP""""
]
ParserVersion = "v1.0.0"
},
  
{
  Name = microsoft-mssql-kv-app-login-fail-18456
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = SQL Server
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """EventCode=18456""", """Keywords=Audit Failure""", """Login failed""" ]
  Fields = [
    """(\\n|\W)ComputerName =({host}[\w\-\.]+)\s*(\\n)?(\w+=|$)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (?i)(AM|PM))""",
    """(\\n|\W)Message=[^=]*?\Wuser\s*'\s*((({domain}[^\\]+)(\\)+))?({user}[^\\]+?)'""",
    """(\\n|\W)SourceName =({service_name}[^=]+?)\s*(\\n)?(\w+=|$)""",
    """SourceName =({app}MSSQL)""",
    """\[CLIENT:\s+({src_ip}[a-fA-F\d:\.]+)\]""",
    """\WReason:\s*({failure_reason}[^:]+?)\s*\[""",
    """source_hostname":"({src_host}[^"]+)""",
    """EventCode=({event_code}\d+)""",
    """({event_name}Login failed)""",
  ]
  DupFields = [ "host->dest_host" 
}
```