#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-alert-trigger-success-processachieved"
Vendor = "SentinelOne"
Product = "Singularity Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
ExtractionType = json
Conditions = [
""""s1domain":"""
""""siteId":"""
""""_time":"""
""""accountId":"""
]
Fields = [
"""exa_json_path=$._time,exa_field_name=time""",
"""exa_json_path=$.threatName,exa_field_name=alert_name""",
"""exa_json_path=$.username,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.lastLoggedInUserName,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.accountName,exa_field_name=account""",
"""exa_json_path=$.primaryDescription,exa_field_name=alert_type""",
"""exa_json_path=$.description,exa_field_name=alert_type""",
"""exa_json_path=$.agentComputerName,exa_regex=^({src_host}[\w\-.]+)$""",
"""exa_json_path=$.computerName,exa_regex=^({src_host}[\w\-.]+)$""",
"""exa_json_path=$.agentIp,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
"""exa_json_path=$.externalIp,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
"""exa_json_path=$.agentOsType,exa_field_name=os""",
"""exa_json_path=$.osName,exa_field_name=os""",
"""exa_json_path=$.fileDisplayName,exa_field_name=file_name""",
"""exa_json_path=$.filePath,exa_field_name=malware_url""",
"""exa_json_path=$.domain,exa_field_name=domain""",
"""exa_json_path=$.uuid,exa_field_name=user_uid""",
"""exa_json_path=$..inet[0],exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
"""exa_json_path=$.mitigationStatus,exa_field_name=alert_severity"""
]
DupFields = [
"file_name->process_name"
"file_path->process_path"
]
ParserVersion = "v1.0.0"


}
```