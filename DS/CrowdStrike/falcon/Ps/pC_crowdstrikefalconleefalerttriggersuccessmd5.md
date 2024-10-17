#### Parser Content
```Java
{
Name = "crowdstrike-falcon-leef-alert-trigger-success-md5"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Suspicious Activity"""
"""|CrowdStrikeDetection|"""
"""CrowdStrike-UserName ="""
"""CrowdStrike-MD5"""
]
Fields = [
"""srcPreNAT=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({event_name}CrowdStrike Detection)"""
"""({alert_name}Suspicious Activity)"""
"""CrowdStrike-Severity=({alert_severity}[^\s]+)"""
"""CrowdStrike-DetectId=({alert_id}[^\s]+)"""
"""CrowdStrike-CommandLine="+({process_command_line}({process_dir}[^\.]+)[\\\/][^"]+)"""
"""CrowdStrike-FilePath=({file_path}[^\s]+)"""
"""CrowdStrike-FileName =({process_name}[^\=]+?)(\s+CrowdStrike-SensorId)"""
"""CrowdStrike-ComputerName =({src_host}[^\s]+)"""
"""CrowdStrike-IOCValue=({file_hash}[^\s]+)"""
"""CrowdStrike-UserName =(N/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""CrowdStrike-ProcessId=({process_guid}\d+)"""
"""CrowdStrike-FalconHostLink=({falcon_host_link}[^\s]+)"""
"""CrowdStrike-MD5=({hash_md5}[^\s]+)"""
]
DupFields = [
"falcon_host_link->additional_info"
"process_command_line->process_path"
]
ParserVersion = "v1.0.0"


}
```