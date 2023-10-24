#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-alert-trigger-success-processachieved"
Vendor = "SentinelOne"
Product = "Singularity Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
""""s1domain":"""
""""siteId":"""
""""_time":"""
""""accountId":"""
]
Fields = [
""""_time":\s*"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""""
""""threatName"+:\s*"+({alert_name}[^"]+)"""
""""(username|lastLoggedInUserName)"+:\s*"+({user}[\w\.\-]{1,40}\$?)"""
""""accountName"+:\s*"+({account}[^"]+)"""
""""(description|primaryDescription)"+:\s*"+({alert_type}[^"]+)"""
""""(computerName|agentComputerName)"+:\s*"+({src_host}[\w\-.]+)""""
""""(agentIp|externalIp)"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""(agentOsType|osName)"+:\s*"+({os}[^"]+)"""
""""fileDisplayName"+:\s*"+({file_name}[^"]+)"""
""""filePath"+:\s*"+({malware_url}[^"]+)"""
""""domain"+:\s*"+({domain}[^",]+)"""
""""uuid"+:\s*"+({user_uid}[^"]+)"""
""""inet":\s*\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"]"""
""""description":\s"({alert_type}[^"]+)"""
"""mitigationStatus":\s"({alert_severity}[^"]+)"""
]
DupFields = [
"file_name->process_name"
"file_path->process_path"
]
ParserVersion = "v1.0.0"


}
```