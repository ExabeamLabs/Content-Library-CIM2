#### Parser Content
```Java
{
Name = "microsoft-mcas-kv-app-login-fail-failedauth"
Conditions = [
"""ACTION: AUTHENTICATION_FAILED"""
"""ACTION: """
"""WHO: """
"""WHEN: """
"""CLIENT IP ADDRESS: """
"""SERVER IP ADDRESS: """
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
     """"InitiatingProcessParentFileName":"({parent_process_name}[^"]+)""""
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
  """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s"""
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
  """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s"""
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

${MicrosoftParserTemplates.json-microsoft-security-events-1}{
Name = microsoft-defenderep-json-alert-trigger-success-lateralmovement
ExtractionType = json
ParserVersion = "v1.0.0"
Conditions = [
  """"category":"""
  """"LateralMovement""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"Microsoft Defender ATP""""
]
Fields = ${MicrosoftParserTemplates.json-microsoft-security-events-1.Fields}[
  """exa_regex="privateIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_regex="publicIpAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$.id,exa_field_name=alert_id"""
  """exa_regex="domainName":\s*"({domain}[^"]+)",\s*"userPrincipalName"""
  """exa_regex="fqdn":\s*"({src_host}[^"]+)"""

}
```