#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-alert-trigger-success-falconhostlink"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""ExternalApiType": "Event_DetectionSummaryEvent""""
""""Severity""""
""""FalconHostLink""""
]
Fields = [
""""ProcessStartTime":\s*({time}\d{10})"""
""""UserName":\s*\"({user}[\w\.\-]{1,40}\$?)(@({src_host}[^\"]+))?\""""
""""ComputerName":\s*\"({src_host}[^\"]+)\""""
""""DetectName":\s*\"({alert_name}[^\"]+)\""""
""""ExternalApiType":\s*\"({alert_type}[^\"]+)\""""
""""DetectDescription":\s*\"({additional_info}[^\"]+)\""""
""""Severity\":\s*({alert_severity}\d+)"""
""""SeverityName\":\s*\"({alert_severity}[^\"]+?)\""""
""""FileName\":\s*\"({file_name}[^\"]+?)\""""
""""FilePath\":\s*\"({file_path}[^\"]+?)\\?\""""
""""CommandLine\"+:\s*\"+\\*\"*({process_command_line}[^\n]+?)\\*\s*\"+,"""
""""CommandLine\":\s*\"\\\"({process_path}({process_dir}[^\",]+\\\\)?({process_name}[^\"\\,]+))\\\""""
""""LocalIP\":\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""RemoteAddress\":\s*\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\\*\"DetectDescription\\*\":\s*\\*\"({alert_name}[^\"]+)"""
""""DetectName\":\s*\"({alert_name}[^\"]+)"""
""""Technique\":\s*\"({alert_type}[^\"]+)"""
""""LocalAddress\":\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""DetectId\"+:\s*\"+({alert_id}[^\"]+)\""""
""""MD5String"+:\s*\"+({hash_md5}[^\"]+)\""""
""""SHA256String":\s*\"({hash_sha256}[^\"]+)"""
""""GrandparentImageFileName\\*\"+:\s*\\*\"+({grandparent_image_filename}[^,]+?)\\*\"+,"""
""""GrandparentCommandLine\\*\"+:\s*\\*\"+({grandparent_command_line}[^,]+?)\\*\"+,"""
""""ParentImageFileName\\*\"+:\s*\\*\"+({parent_image_filename}[^,]+?)\\*\"+,"""
""""ParentCommandLine\\*\"+:\s*\\*\"+({parent_process_command_line}[^,]+?)\"+,"""
""""PatternDispositionDescription\\*\"+:\s*\\*\"+({pattern_disposition_description}[^\"]+)"""
""""FalconHostLink\\*\"+:\s*\\*\"+({falcon_host_link}[^\"]+)"""
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
""""cid":"({cid}[^"]+)"""
]
DupFields = [
"falcon_host_link->additional_info"
]
ParserVersion = "v1.0.0"


}
```