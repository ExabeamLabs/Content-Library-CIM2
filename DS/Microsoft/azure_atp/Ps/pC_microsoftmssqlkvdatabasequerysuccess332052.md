#### Parser Content
```Java
{
Name = microsoft-mssql-kv-database-query-success-33205-2
Conditions = [
  """EventCode=33205"""
  """action_id:AL"""
]
ParserVersion = "v1.0.0"

cef-defender-atp-2.Fields} [
     """ProcessId":({process_id}\d+)""",
     """InitiatingProcessFileName":\s*"({process_name}[^"]+)""",
     """"FileName":"({file_name}[^"]+?(\.({file_ext}[^".]+))?)"""",
     """"FolderPath":"({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
     """DeviceName":\s*"({dest_host}[\w\-.]+)""",
     """ProcessCommandLine":\s*"({process_command_line}[^"]+)\s*""""
     """MD5":"({hash_md5}[^"]+)""",
     """"InitiatingProcessMD5":"({hash_md5}[^"]+)"""",
     """"SHA256":"({hash_sha256}[^",]+)",""",
     """"InitiatingProcessSHA256":"({hash_sha256}[^",]+)",""",
     """"SHA1":"({hash_sha1}[^"]+)"""",
     """"InitiatingProcessSHA1":"({hash_sha1}[^"]+)"""",
     """"InitiatingProcessParentFileName":"({parent_process}[^"]+)""""
 ]
 ParserVersion = "v1.0.0"
},

{
Vendor = Microsoft
Product = Azure ATP
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
  """\Wsuser=({user}[\w\.\-]{1,40}\$?)\s"""
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
Product = Azure ATP
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
  """CEF:?([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({event_code}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wshost=(({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({src_host}[\w\-.]+))"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wcs1=({malware_url}.+?)\s+(\w+=|$).+?cs1Label=url"""
  """\Wcs1Label=url.*?\Wcs1=({malware_url}.+?)\s+(\w+=|$)"""
  """\Wsuser=({user}[\w\.\-]{1,40}\$?)\s"""
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
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Fields = [
  """"id":\s*"({alert_id}[^"]+)""""
  """"title":\s*"({alert_name}[^"]+)""""
  """"severity":\s*"({alert_severity}[^"]+)""""
  """"category":\s*"({alert_type}[^"]+)""""
  """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]"""
  """"sourceMaterials":\["({additional_info}[^"]+)"""",
  """"eventDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)""""
  """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[\w\.\-]{1,40}\$?))""""
  """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[\w\.\-]{1,40}\$?))""""
  """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-]{1,40}\$?)(@[^"]+)?))""""
  """"userPrincipalName":\s*"({user_upn}[^"]+?)""""
  """"domainName"+:\s*"+(-|({domain}[^"]+))""""
  """"domainName"+:\s*"+(-|({domain}[^"]+))[^}\]]+?userPrincipalName"""
  """"fqdn"+:\s*"+({src_host}[^"]+)""""
  """"+hostStates"+:[^}\]]+?privateIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"+hostStates"+:[^}\]]+?publicIpAddress"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"description":\s*"An actor on\s*({src_host}\S+)\s*performed suspicious"""
  """"fileStates":[^]]+?"name":\s*"({file_name}[^."]+([\.\w]+)?)""""
  """"destinationServiceName":"({app}[^"]+)""""
]
Name = microsoft-defenderep-json-alert-trigger-success-lateralmovement
Product = Microsoft Defender for Endpoint
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
  Product = MSSQL
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """EventCode=18456""", """Keywords=Audit Failure""", """Login failed""" ]
  Fields = [
    """(\\n|\W)ComputerName =({host}[\w\-\.]+)\s*(\\n)?(\w+=|$)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (?i)(AM|PM))""",
    """(\\n|\W)Message=[^=]*?\Wuser\s*'\s*((({domain}[^\\]+)(\\)+))?({user}[\w\.\-]{1,40}\$?)'""",
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