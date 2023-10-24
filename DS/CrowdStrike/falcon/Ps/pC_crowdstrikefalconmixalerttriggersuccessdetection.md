#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-alert-trigger-success-detection"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""eventType":"""
""""DetectionSummaryEvent""""
]
Fields = [
""""eventCreationTime":\s*({time}\d{10})"""
""""DetectName":\s*"({alert_type}[^"]+)"""
""""Technique":"({alert_name}[^"]+)""""
""""SeverityName":"({alert_severity}[^"]+?)""""
""""Severity":\s*({alert_severity}[^",]+)"""
""""DetectId":\s*"({alert_id}[^"]+)"""
"""({additional_info_1}"DocumentsAccessed":\s*[^\]]+\]).*?({additional_info_2}"ExecutablesWritten":\s*[^\]]+\])"""
""""FileName":\s*"\s*({process_name}[^"]+?)""""
""""FilePath":\s*"(|({file_path}[^"]+))""""
""""CommandLine"+:\s*"+\\*"*\s*({process_command_line}[^\n]+?)\\*\s*"+,"""
""""SensorId":\s*"({sensor_id}[^"]+)"""
""""ComputerName":\s*"({src_host}[^"]+)"""
""""LocalIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""ComputerName":\s*"({src_host}[^"]+)".*?"LocalAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","LocalPort":\s*({=src_port}\d+),"RemoteAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","RemotePort":\s*({=dest_port}\d+),"ConnectionDirection":\s*0"""
""""ComputerName":\s*"({dest_host}[^"]+)".*?"LocalAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","LocalPort":\s*({=dest_port}\d+),"RemoteAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","RemotePort":\s*({=src_port}\d+),"ConnectionDirection":\s*1"""
""""IOCValue":\s*"({ioc}[^"]+)""""
""""MD5String":\s*"(|({hash_md5}[^"]+))""""
""""UserName":\s*"(N/A|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""""
""""FalconHostLink":\s*"({falcon_host_link}[^"]+)""""
""""DetectDescription":\s*"\s*({alert_description}[^"]+?)\s*""""
""""GrandparentImageFileName\\*"+:\s*\\*"+({grandparent_image_filename}[^,]+?)\\*"+,"""
""""GrandparentCommandLine\\*"+:\s*\\*"+({grandparent_command_line}[^

}
```