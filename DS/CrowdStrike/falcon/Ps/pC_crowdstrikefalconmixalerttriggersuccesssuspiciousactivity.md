#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-alert-trigger-success-suspiciousactivity"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""eventType":""""
""""DetectionSummaryEvent""""
""""DetectName":""""
""""Suspicious Activity""""
]
Fields = [
""""eventCreationTime":\s*({time}\d{10})"""
""""Tactic":"({category}[^"]+)""""
""""DetectName":\s*"({alert_type}[^"]+)""""
""""DetectDescription":"({alert_name}[^"]+)""""
""""IOARuleName":"({alert_name}[^"]+)""""
""""Severity":\s*({alert_severity}[^",]+)"""
""""SeverityName":"({alert_severity}[^"]+?)""""
""""DetectId":\s*"({alert_id}[^"]+)""""
""""Technique":"({alert_type}[^"]+)"""
"""({additional_info_1}"DocumentsAccessed":\s*[^\]]+\]).*?({additional_info_2}"ExecutablesWritten":\s*[^\]]+\])"""
""""CommandLine":"({process_path}({process_dir}[^\s]+)\\\\({process_name}[^\s]+))"""
""""CommandLine":"\\"({process_path}({process_dir}[^"]+?)\\{1,2}({process_name}[^\\"]+))\\""""
""""FileName":\s*"({process_name}[^"]+)""""
""""FilePath":\s*"({file_path}[^"]+)""""
""""CommandLine":"({process_command_line}[^,]+?)\\?",""""
""""SensorId":\s*"({sensor_id}[^"]+)""""
""""ComputerName":\s*"({src_host}[^"]+)""""
""""LocalIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""ComputerName":\s*"({src_host}[^"]+)".*?"LocalAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","LocalPort":\s*({=src_port}\d+),"RemoteAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","RemotePort":\s*({=dest_port}\d+),"ConnectionDirection":\s*0"""
""""ComputerName":\s*"({dest_host}[^"]+)".*?"LocalAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","LocalPort":\s*({=dest_port}\d+),"RemoteAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","RemotePort":\s*({=src_port}\d+),"ConnectionDirection":\s*1"""
""""PatternDispositionDescription":"({additional_info}[^"]+)""""
""""MD5String":\s*"({hash_md5}[^"]+)""""
""""UserName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""""
""""ProcessId":({process_guid}\d+)"""
""""ParentProcessId":({parent_process_guid}\d+)"""
""""FalconHostLink":\s*"({falcon_host_link}[^"]+)""""
""""((?i)SHA256|SHA256String|SHA256HashData)\\*"+:\s*\\*"+({hash_sha256}[^,]+?)\\*"+,"""
""""GrandparentImageFileName\\*":\\*"({grandparent_image_filename}[^,]+?)\\*"+"""
""""GrandparentCommandLine\\*"+:\s*\\*"+({grandparent_command_line}[^,]+?)\\*"+,"""
""""ParentImageFileName\\*":\s*\\*"({parent_image_filename}[^,]+?)\\*"+,"""
""""ParentCommandLine\\*":\s*\\*"({parent_process_command_line}[^,]+?)\s*"+,"""
""""PatternDispositionFlags":\{({disposition}[^\}]+?)\}"""
""""LocalAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({src_port}\d+)".+?"ConnectionDirection":"0""""
""""LocalAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({dest_port}\d+)".+?"ConnectionDirection":"1""""
""""RemoteAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({dest_port}\d+)".+?"ConnectionDirection":"0""""
""""RemoteAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({src_port}\d+)".+?"ConnectionDirection":"1""""
""""RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":({dest_port}\d+),.+?"Protocol":"({protocol}[^"]+)",.+?"ConnectionDirection""""
""""destinationServiceName":"({alert_source}[^"]+)""""
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