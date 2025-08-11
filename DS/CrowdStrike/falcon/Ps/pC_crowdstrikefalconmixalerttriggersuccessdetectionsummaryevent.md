#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-alert-trigger-success-detectionsummaryevent"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","epoch_sec"]
Conditions = [
""""ExternalApiType":"Event_DetectionSummaryEvent""""
""""Severity""""
""""FalconHostLink""""
]
Fields = [
""""ProcessStartTime":({time}\d{10})"""
"""({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)"""
""""Tactic":"({category}[^"]+)""""
""""UserName":"(N/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({src_host}[^"]+))?""""
""""ComputerName":"({src_host}[^"]+)""""
"""\\*"DetectDescription\\*":\\*"({alert_name}[^"]+?)(\.\s+|")"""
""""DetectName":"({alert_type}[^"]+)""""
""""IOARuleName":"({alert_name}[^"]+)""""
""""ExternalApiType":"({alert_type}[^"]+)""""
""""DetectDescription":"({additional_info}[^"]+)""""
""""PatternDispositionDescription":"({additional_info}[^"]+)""""
""""Severity":\s*({alert_severity}\d+)"""
""""SeverityName":\s*"({alert_severity}[^"]+?)""""
""""FileName":"({file_name}[^"]+?)""""
""""FilePath":"({file_dir}[^"]+?)\\?""""
""""CommandLine"+:"+\\*"*({process_command_line}[^,"]+?)\\*""""
""""CommandLine"+:"+\\*"*({process_path}({process_dir}[^",]+\\\\)?({process_name}[^"\\,]+))\\*""""
""""LocalIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""IOCValue":\s*"(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({domain}[a-zA-Z\.\-]+))""""
""""Technique":"({alert_type}[^"]+)"""
""""LocalAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""DetectId"+:"+({alert_id}[^"]+)""""
""""MD5String"+:"+({hash_md5}[^",]+)""""
""""SHA256String":"({hash_sha256}[^",]+)"""
"""SensorId":"({sensor_id}[^"]+)"""
""""GrandparentImageFileName\\*":\\*"({grandparent_image_filename}[^,]+?)\\*"+"""
""""GrandparentCommandLine\\*"+:\s*\\*"+({grandparent_command_line}[^,]+?)\\*"+,"""
""""ParentImageFileName\\*":\s*\\*"({parent_image_filename}[^,]+?)\\*"+,"""
""""ParentCommandLine\\*":\s*\\*"({parent_process_command_line}[^,]+?)"+,"""
""""PatternDispositionDescription\\*":\s*\\*"({pattern_disposition_description}[^"]+)"""
""""FalconHostLink\\*":\s*\\*"({falcon_host_link}[^"]+)"""
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
""""cid":"({cid}[^"]+)"""
""""customerIDString":"({cid}[^"]+)""""
"""exa_json_path=$..cid,exa_field_name=cid""",
"""exa_json_path=$..customerIDString,exa_field_name=cid""",
"""exa_json_path=$.ProcessStartTime,exa_field_name=time""",
"""exa_regex=({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)""",
"""exa_json_path=$.Tactic,exa_field_name=category""",
"""exa_json_path=$.UserName,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({src_host}[^\"]+))?""",
"""exa_json_path=$.ComputerName,exa_field_name=src_host""",
"""exa_json_path=$.DetectDescription,exa_field_name=alert_name""",
"""exa_json_path=$.DetectName,exa_field_name=alert_type""",
"""exa_json_path=$.IOARuleName,exa_field_name=alert_name""",
"""exa_json_path=$.ExternalApiType,exa_field_name=alert_type""",
"""exa_json_path=$.DetectDescription,exa_field_name=additional_info""",
"""exa_json_path=$.PatternDispositionDescription,exa_field_name=additional_info""",
"""exa_json_path=$.Technique,exa_field_name=alert_type""",
"""exa_json_path=$.IOCValue,exa_regex=^(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({domain}[a-zA-Z\.\-]+))$""",
"""exa_json_path=$.DetectId,exa_field_name=alert_id""",
"""exa_json_path=$.Severity,exa_field_name=severity""",
"""exa_json_path=$.SeverityName,exa_field_name=alert_severity""",
"""exa_json_path=$.FileName,exa_field_name=file_name""",
"""exa_json_path=$.FilePath,exa_field_name=file_dir""",
"""exa_regex="CommandLine\"+:\s*\"+\\*\"*({process_command_line}[^\n]+?)\\*\s*\"+,""",
"""exa_regex="CommandLine\":\s*\"\\\"({process_path}({process_dir}[^\",]+\\\\)?({process_name}[^\"\\,]+))\\\"""",
"""exa_json_path=$.LocalIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.LocalAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.LocalPort,exa_field_name=src_port""",
"""exa_json_path=$.RemoteAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
"""exa_json_path=$.RemotePort,exa_field_name=dest_port""",
"""exa_json_path=$.MD5String,exa_field_name=hash_md5""",
"""exa_json_path=$.SHA256String,exa_field_name=hash_sha256""",
"""exa_regex=SensorId":"({sensor_id}[^"]+)""",
"""exa_json_path=$.GrandparentImageFileName,exa_field_name=grandparent_image_filename""",
"""exa_json_path=$.GrandparentCommandLine,exa_field_name=grandparent_command_line""",
"""exa_json_path=$.ParentImageFileName,exa_field_name=parent_image_filename""",
"""exa_json_path=$.ParentCommandLine,exa_field_name=parent_process_command_line""",
"""exa_json_path=$.FalconHostLink,exa_field_name=falcon_host_link""",
"""exa_json_path=$.PatternDispositionFlags.BootupSafeguardEnabled,exa_field_name=bootup_safeguard_enabled""",
"""exa_json_path=$.PatternDispositionFlags.QuarantineFile,exa_field_name=quarantine_file""",
"""exa_json_path=$.PatternDispositionFlags.QuarantineMachine,exa_field_name=quarantine_machine""",
"""exa_json_path=$.PatternDispositionFlags.Detect,exa_field_name=detect""",
"""exa_json_path=$.PatternDispositionFlags.RegistryOperationBlocked,exa_field_name=registry_operation_blocked""",
"""exa_json_path=$.PatternDispositionFlags.KillParent,exa_field_name=kill_parent""",
"""exa_json_path=$.PatternDispositionFlags.FsOperationBlocked,exa_field_name=fs_operation_blocked""",
"""exa_json_path=$.PatternDispositionFlags.OperationBlocked,exa_field_name=operation_blocked""",
"""exa_json_path=$.PatternDispositionFlags.KillProcess,exa_field_name=kill_process""",
"""exa_json_path=$.PatternDispositionFlags.ProcessBlocked,exa_field_name=process_blocked""",
"""exa_json_path=$.PatternDispositionFlags.PolicyDisabled,exa_field_name=policy_disabled""",
"""exa_json_path=$.PatternDispositionFlags.SensorOnly,exa_field_name=sensor_only""",
"""exa_json_path=$.PatternDispositionFlags.CriticalProcessDisabled,exa_field_name=rcritical_process_disabled""",
"""exa_json_path=$.PatternDispositionFlags.KillSubProcess,exa_field_name=kill_sub_process""",
"""exa_json_path=$.PatternDispositionFlags.Rooting,exa_field_name=rooting""",
"""exa_json_path=$.PatternDispositionFlags.InddetMask,exa_field_name=inddet_mask""",
"""exa_json_path=$.PatternDispositionFlags.Indicator,exa_field_name=indicator""",
]
DupFields = [
"alert_type->technique"
"falcon_host_link->additional_info"
]
ParserVersion = "v1.0.0"


}
```