#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-alert-trigger-success-annotation"
Vendor = "SentinelOne"
Product = "Singularity Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
""""annotation": """
""""threatName": """"
""""fileContentHash": """"
""""fileExtensionType": """"
""""s1domain": """"
]
Fields = [
""""_time":\s*"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""
""""username":\s*"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-]{1,40}\$?)""""
""""classification":\s*"({alert_type}[^"]+)"""
""""filePath":\s*"({malware_url}[^"]+)"""
""""fileContentHash":\s*"({hash_sha1}[^"]+)"""
""""rank":\s*(null|({alert_severity}[^",]+))"""
""""agentDomain":\s*"({src_domain}[^"]+)"""
""""agentComputerName":\s*"({src_host}[^"]+)"""
""""fileExtensionType":\s*"(None|Unknown|({file_type}[^"]+))"""
""""agentOsType":\s*"({os}[^"]+)"""
""""annotation":\s*"({additional_info}[^"]+)"""
""""threatName":\s*"({alert_name}[^"]+)"""
""""agentIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""fileDisplayName":\s"({file_name}[^"]+)"""
]
DupFields = [
"file_name->process_name"
"malware_url->process_path"
]
ParserVersion = "v1.0.0"


}
```