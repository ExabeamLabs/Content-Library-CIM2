#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-alert-trigger-success-detection"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = ["epoch_sec","epoch"]
Conditions = [
""""eventType":"""
"""DetectionSummaryEvent""""
]
Fields = [
""""eventCreationTime":\s*({time}\d{10})"""
""""DetectName":\s*"({alert_type}[^"]+)"""
""""Technique":"({alert_subject}({alert_name}[^"]+))""""
""""Severity":\s*({alert_severity}[^",]+)"""
""""SeverityName":\s*"({alert_severity}[^"]+?)""""
""""DetectId":\s*"({alert_id}[^"]+)"""
"""({additional_info_1}"DocumentsAccessed":\s*[^\]]+\]).*?({additional_info_2}"ExecutablesWritten":\s*[^\]]+\])"""
""""FileName":\s*"\s*({process_name}[^"]+?)""""
""""CommandLine"+:\s*"+\\*"*\s*({process_command_line}[^\n]+?)\\*\s*"+,"""
""""SensorId":\s*"({sensor_id}[^"]+)"""
""""ComputerName":\s*"({src_host}[\w\-.]+)"""
""""LocalIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""ComputerName":\s*"({src_host}[\w\-.]+)".*?"LocalAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","LocalPort":\s*({=src_port}\d+),"RemoteAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","RemotePort":\s*({=dest_port}\d+),"ConnectionDirection":\s*0"""
""""ComputerName":\s*"({dest_host}[\w\-.]+)".*?"LocalAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","LocalPort":\s*({=dest_port}\d+),"RemoteAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","RemotePort":\s*({=src_port}\d+),"ConnectionDirection":\s*1"""
""""IOCValue":\s*"({ioc}[^"]+)""""
""""MD5String":\s*"(|({hash_md5}[^"]+))""""
""""UserName":\s*"(N/A|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
""""FalconHostLink":\s*"({malware_url}({falcon_host_link}[^"]+))""""
""""DetectDescription":\s*"\s*({additional_info}({alert_description}[^"]+?))\s*""""
""""GrandparentImageFileName\\*"+:\s*\\*"+({grandparent_image_filename}[^,]+?)\\*"+,"""
""""GrandparentCommandLine\\*"+:\s*\\*"+({grandparent_command_line}[^},]+?)\\*\s*"+(,|})"""
""""ParentImageFileName\\*"+:\s*\\*"+({parent_image_filename}[^,]+?)\\*"+,"""
""""ParentCommandLine\\*"+:\s*\\*"+({parent_process_command_line}[^,]+?)\s*"+,"""
""""((?i)SHA256|SHA256String|SHA256HashData)\\*"+:\s*\\*"+({hash_sha256}[^,]+?)\\*"+,"""
""""PatternDispositionDescription\\*"+:\s*\\*"+({pattern_disposition_description}[^"]+)""",
""""BootupSafeguardEnabled":\s*({bootup_safeguard_enabled}true|false)"""
""""QuarantineFile"+:\s*({quarantine_file}true|false)"""
""""QuarantineMachine"+:\s*({quarantine_machine}true|false)"""
""""Detect"+:\s*({detect}true|false)"""
""""RegistryOperationBlocked"+:\s*({registry_operation_blocked}true|false)"""
""""KillParent"+:\s*({kill_parent}true|false)"""
""""FsOperationBlocked"+:\s*({fs_operation_blocked}true|false)"""
""""OperationBlocked"+:\s*({operation_blocked}true|false)"""
""""KillProcess"+:\s*({kill_process}true|false)"""
""""ProcessBlocked"+:\s*({process_blocked}true|false)"""
""""PolicyDisabled"+:\s*({policy_disabled}true|false)"""
""""SensorOnly"+:\s*({sensor_only}true|false)"""
""""CriticalProcessDisabled"+:\s*({critical_process_disabled}true|false)"""
""""KillSubProcess"+:\s*({kill_sub_process}true|false)"""
""""Rooting"+:\s*({rooting}true|false)"""
""""InddetMask"+:\s*({inddet_mask}true|false)"""
""""Indicator"+:\s*({indicator}true|false)"""
""""aid":"({aid}[^"]+)"""
""""PatternDispositionFlags":\{({disposition}[^\}]+?)\}"""
""""LocalAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({src_port}\d+)".+?"ConnectionDirection":"0"""",
""""LocalAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({dest_port}\d+)".+?"ConnectionDirection":"1"""",
""""RemoteAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({dest_port}\d+)".+?"ConnectionDirection":"0"""",
""""RemoteAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({src_port}\d+)".+?"ConnectionDirection":"1""""
""""RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":({dest_port}\d+),.+?"Protocol":"({protocol}[^"]+)",.+?"ConnectionDirection""""
""""ComputerName":\s*"({dest_host}[\w\-\.]+)"""
""""FileName":\s*"({file_name}[^"]+?(\.({file_ext}\w+))?)","""
""""FilePath":\s*"(|(({file_dir}[^"]+?[\\\/]+)({file_name}[^"\\\/]+(\.({file_ext}[a-zA-Z]+))))|({=file_dir}[^"]+))""""
""""Files(Written|Accessed)":\[\{[^\}]*"FileName":"({file_name}.*?(\.({file_ext}\w{3,7}))?)","FilePath":"({file_dir}[^"]+)"\}"""
""""destinationServiceName":"({alert_source}[^"]+)""""
""""Description":"({additional_info}[^"]+)""""
""""Hostname":\s*"({src_host}[\w\-\.]+)"""
""""AgentId":"({aid}[^"]+)"""
""""cid":"({cid}[^"]+)""""
""""customerIDString":"({cid}[^"]+)""""
"""exa_json_path=$..cid,exa_field_name=cid""",
"""exa_json_path=$..customerIDString,exa_field_name=cid""",
"""exa_json_path=$..Hostname,exa_regex=^({src_host}[\w\-.]+)$"""
"""exa_json_path=$..AgentId,exa_field_name=aid"""
"""exa_json_path=$.metadata.eventCreationTime,exa_field_name=time""",
"""exa_json_path=$..eventType,exa_field_name=event_category""",
"""exa_json_path=$..DetectName,exa_field_name=alert_type""",
"""exa_json_path=$..Technique,exa_field_name=alert_name""",
"""exa_json_path=$..Technique,exa_field_name=alert_subject""",
"""exa_json_path=$..Severity,exa_field_name=alert_severity""",
"""exa_json_path=$..SeverityName,exa_field_name=alert_severity""",
"""exa_json_path=$..DetectId,exa_field_name=alert_id""",
"""exa_regex=({additional_info_1}"DocumentsAccessed":\s*[^\]]+\]).*?({additional_info_2}"ExecutablesWritten":\s*[^\]]+\])""",
"""exa_json_path=$.event.FileName,exa_field_name=process_name""",
"""exa_json_path=$..CommandLine,exa_field_name=process_command_line""",
"""exa_json_path=$..SensorId,exa_field_name=sensor_id""",
"""exa_json_path=$.event.ComputerName,exa_regex=^({src_host}[\w\-.]+)$""",
"""exa_json_path=$..LocalIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_regex="ComputerName":\s*"({src_host}[\w\-.]+)".*?"LocalAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","LocalPort":\s*({=src_port}\d+),"RemoteAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","RemotePort":\s*({=dest_port}\d+),"ConnectionDirection":\s*0""",
"""exa_regex="ComputerName":\s*"({dest_host}[\w\-.]+)".*?"LocalAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","LocalPort":\s*({=dest_port}\d+),"RemoteAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","RemotePort":\s*({=src_port}\d+),"ConnectionDirection":\s*1""",
"""exa_json_path=$..IOCValue,exa_field_name=ioc""",
"""exa_json_path=$..MD5String,exa_field_name=hash_md5""",
"""exa_json_path=$..UserName,exa_regex=(N/A|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
"""exa_json_path=$..FalconHostLink,exa_field_name=falcon_host_link""",
"""exa_json_path=$..FalconHostLink,exa_field_name=malware_url""",
"""exa_json_path=$..DetectDescription,exa_field_name=alert_description""",
"""exa_json_path=$..DetectDescription,exa_field_name=additional_info""",
"""exa_json_path=$..GrandparentImageFileName,exa_field_name=grandparent_image_filename""",
"""exa_json_path=$..GrandparentCommandLine,exa_field_name=grandparent_command_line""",
"""exa_json_path=$..ParentImageFileName,exa_field_name=parent_image_filename""",
"""exa_json_path=$..ParentCommandLine,exa_field_name=parent_process_command_line""",
"""exa_regex="((?i)SHA256|SHA256String|SHA256HashData)\\*"+:\s*\\*"+({hash_sha256}[^,]+?)\\*"+,""",
"""exa_json_path=$..PatternDispositionDescription,exa_field_name=pattern_disposition_description""",
"""exa_json_path=$..PatternDispositionFlags.BootupSafeguardEnabled,exa_field_name=bootup_safeguard_enabled""",
"""exa_json_path=$..PatternDispositionFlags.QuarantineFile,exa_field_name=quarantine_file""",
"""exa_json_path=$..PatternDispositionFlags.QuarantineMachine,exa_field_name=quarantine_machine""",
"""exa_json_path=$..PatternDispositionFlags.Detect,exa_field_name=detect""",
"""exa_json_path=$..PatternDispositionFlags.RegistryOperationBlocked,exa_field_name=registry_operation_blocked""",
"""exa_json_path=$..PatternDispositionFlags.KillParent,exa_field_name=kill_parent""",
"""exa_json_path=$..PatternDispositionFlags.FsOperationBlocked,exa_field_name=fs_operation_blocked""",
"""exa_json_path=$..PatternDispositionFlags.OperationBlocked,exa_field_name=operation_blocked""",
"""exa_json_path=$..PatternDispositionFlags.KillProcess,exa_field_name=kill_process""",
"""exa_json_path=$..PatternDispositionFlags.ProcessBlocked,exa_field_name=process_blocked""",
"""exa_json_path=$..PatternDispositionFlags.PolicyDisabled,exa_field_name=policy_disabled""",
"""exa_json_path=$..PatternDispositionFlags.SensorOnly,exa_field_name=sensor_only""",
"""exa_json_path=$..PatternDispositionFlags.CriticalProcessDisabled,exa_field_name=rcritical_process_disabled""",
"""exa_json_path=$..PatternDispositionFlags.KillSubProcess,exa_field_name=kill_sub_process""",
"""exa_json_path=$..PatternDispositionFlags.Rooting,exa_field_name=rooting""",
"""exa_json_path=$..PatternDispositionFlags.InddetMask,exa_field_name=inddet_mask""",
"""exa_json_path=$..PatternDispositionFlags.Indicator,exa_field_name=indicator""",
"""exa_json_path=$..aid,exa_field_name=aid""",
"""exa_json_path=$..PatternDispositionFlags,exa_regex=\{({disposition}[^\}]+?)\}""",
"""exa_regex="LocalAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({src_port}\d+)".+?"ConnectionDirection":"0"""",
"""exa_regex="LocalAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({dest_port}\d+)".+?"ConnectionDirection":"1"""",
"""exa_regex="RemoteAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({dest_port}\d+)".+?"ConnectionDirection":"0"""",
"""exa_regex="RemoteAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({src_port}\d+)".+?"ConnectionDirection":"1"""",
"""exa_regex="RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":({dest_port}\d+),.+?"Protocol":"({protocol}[^"]+)",.+?"ConnectionDirection"""",
"""exa_json_path=$.event.ComputerName,exa_regex=^({dest_host}[\w\-.]+)$""",
"""exa_regex="destinationServiceName":"({alert_source}[^"]+)""""
"""exa_json_path=$..Name,exa_field_name=alert_name"""
"""exa_json_path=$..Name,exa_field_name=alert_subject"""
"""exa_json_path=$.SourceAccountName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""exa_json_path=$.UTCTimestamp,exa_field_name=time"""
"""exa_regex="FileName":\s*"({file_name}[^"]+?(\.({file_ext}\w+))?)","""
"""exa_json_path=$.event.FilePath,exa_regex=^(|({file_path}({file_dir}[^"]+?[\\\/]+)({file_name}[^"\\\/]+(\.({file_ext}[a-zA-Z]+))))|({=file_dir}[^"]+))$""",
"""exa_regex="Files(Written|Accessed)":\[\{[^\}]*"FileName":"({file_name}.*?(\.({file_ext}\w{3,7}))?)","FilePath":"({file_dir}[^"]+)"\}"""
"""exa_json_path=$..Hostname,exa_regex=^({host}[\w\-.]+)$"""
"""exa_json_path=$.event.Hostname,exa_regex=^({host}[\w\-.]+)$"""
"""exa_json_path=$.event.SourceProducts,exa_field_name=src_product"""
"""exa_json_path=$.event.SourceEndpointIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.event.SourceEndpointHostName,exa_regex=^({src_host}[\w\-.]+)$"""
"""exa_json_path=$.event.SourceAccountDomain,exa_field_name=domain"""
""""SourceAccountDomain":"({domain}[^"]+)"""",
""""SourceEndpointHostName":"({src_host}[\w\-.]+)"""",
""""SourceEndpointIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
""""SourceProducts":"({src_product}[^"]+)"""",
""""SourceAccountName":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"""time->startedDate"""
"""vendor->source"""
"""rawLog->sourceInfo"""
"""alert_name->malwareName"""
"""alert_type->malwareCategory"""
"""alert_severity->sourceSeverity"""
"""src_host->malwareVictimHost"""
"""malware_url->malwareAttackerFile"""
"""dest_ip->malwareAttackerIp"""
  ]
  NameTemplate = "CrowdStrike Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
"""src_ip->ip_address"""
      ]
    

}
```