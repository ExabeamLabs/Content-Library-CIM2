#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-alert-trigger-success-eventtype
  ParserVersion = "v1.0.0"
  Conditions = [ """"s1ql":""", """"eventType":""", """"incidentStatus":""", """"hitType":""", """"severity":""" ]
  Fields = ${SentinelOneParsersTemplates.sentinelone-json-api-alerts.Fields} [
    """exa_json_path=$.alertInfo.indicatorDescription,exa_field_name=additional_info""",
    """exa_json_path=$.alertInfo.eventType,exa_field_name=alert_name""",
    """exa_json_path=$.ruleInfo.name,exa_field_name=alert_type""",
    """exa_json_path=$..severity,exa_field_name=alert_severity""",
    """exa_json_path=$..incidentStatus,exa_field_name=incident_status"""
  ]
  DupFields = [ "alert_name->alert_subject" ]

sentinelone-json-api-alerts {
    Vendor = SentinelOne
    Product = Singularity Platform
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    ExtractionType = json
    Fields = [
      """exa_json_path=$..createdAt,exa_field_name=time""",
      """exa_json_path=$.sourceProcessInfo.user,exa_regex=(({domain}[^\"\\]+)\\{1,2})?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """exa_json_path=$..eventType,exa_field_name=event_name""",
      """exa_json_path=$..srcIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$..srcPort,exa_field_name=src_port""",
      """exa_json_path=$..dstIp,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """exa_json_path=$..dstPort,exa_field_name=dest_port""",
      """exa_json_path=$..os,exa_field_name=os""",
      """exa_json_path=$.agentDetectionInfo.name,exa_field_name=src_host""",
      """exa_json_path=$.sourceProcessInfo.commandline,exa_field_name=process_command_line""",
      """exa_json_path=$.sourceProcessInfo.name,exa_field_name=process_name""",
      """exa_json_path=$.sourceParentProcessInfo.commandline,exa_field_name=parent_process_command_line""",
      """exa_json_path=$.sourceParentProcessInfo.name,exa_field_name=parent_process_name""",
      """exa_json_path=$.sourceProcessInfo.filePath,exa_field_name=file_path""",
      """exa_json_path=$.sourceProcessInfo.name,exa_field_name=file_name""",
      """exa_json_path=$.sourceProcessInfo.fileHashSha1,exa_field_name=hash_sha1""",
      """exa_json_path=$.sourceProcessInfo.fileHashMd5,exa_field_name=hash_md5""",
      """exa_json_path=$.sourceProcessInfo.fileHashSha256,exa_field_name=hash_sha256""" 
    ] 
  
}
```