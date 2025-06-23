#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-alert-trigger-success-annotation"
Vendor = "SentinelOne"
Product = "Singularity Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
ExtractionType = json
Conditions = [
""""annotation": """
""""threatName": """"
""""fileContentHash": """"
""""fileExtensionType": """"
""""s1domain": """"
]
Fields = [
"""exa_regex="_time":\s*"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
"""exa_regex="username":\s*"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
"""exa_regex="classification":\s*"({alert_type}[^"]+)"""
"""exa_regex="filePath":\s*"({malware_url}[^"]+)"""
"""exa_regex="fileContentHash":\s*"(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))""""
"""exa_regex="rank":\s*(null|({alert_severity}[^",]+))"""
"""exa_regex="agentDomain":\s*"({src_domain}[^"]+)"""
"""exa_regex="agentComputerName":\s*"({src_host}[^"]+)"""
"""exa_regex="fileExtensionType":\s*"(None|Unknown|({file_type}[^"]+))"""
"""exa_regex="agentOsType":\s*"({os}[^"]+)"""
"""exa_regex="annotation":\s*"({additional_info}[^"]+)"""
"""exa_regex="threatName":\s*"({alert_name}[^"]+)"""
"""exa_regex="agentIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_regex="fileDisplayName":\s"({file_name}[^"]+)"""

]
DupFields = [
"file_name->process_name"
"malware_url->process_path"
]
ParserVersion = "v1.0.0"


}
```