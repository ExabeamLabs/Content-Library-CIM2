#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-file-delete-success-deletionfile
  ExtractionType = json
  Product = Singularity Platform
  ParserVersion = v1.0.0
  Conditions = [ """"eventType": "File Deletion"""", """"agentName":""", """"fileFullName":""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-threat-events.Fields}[
    """exa_json_path=$.fileSha1,exa_field_name=hash_sha1""",
  ]

json-sentinelone-threat-events = {
    Vendor = SentinelOne
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [
      """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""",
      """"eventType":\s*"({event_name}[^"]+)"""",
      """"agentName":\s*"({dest_host}[^"]+)"""",
      """"fileFullName":\s*"({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))"""",
      """"processName":\s*"({process_name}[^"]+)"""",
      """"dstIp":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """"srcIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"processUser":\s*"(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """"agentDomain":\s*"({src_domain}[^"]+)""",
      """"agentComputerName":\s*"({src_host}[^"]+)"""
      
      """exa_json_path=$..timestamp,exa_field_name=time""",
      """exa_json_path=$..eventType,exa_field_name=event_name""",
      """exa_json_path=$..agentName,exa_field_name=dest_host""",
      """exa_json_path=$..processName,exa_field_name=process_name""",
      """exa_json_path=$..agentDomain,exa_field_name=src_domain""",
      """exa_json_path=$..agentComputerName,exa_field_name=src_host""",
      """exa_json_path=$..dstIp,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """exa_json_path=$..srcIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$..fileFullName,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))$""",
    
}
```