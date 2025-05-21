#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-alert-trigger-success-rulename"
Vendor = "SentinelOne"
Product = "Singularity Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
ExtractionType = json
Conditions = [
""""rulename":"""
""""activityType":"""
""""ruleid":"""
""""Alert created for """
]
Fields = [
"""exa_json_path=$..origagentname,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$.createdAt,exa_field_name=time""",
"""exa_json_path=$.data.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.data.srcip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
"""exa_json_path=$.data.dstip,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
"""exa_json_path=$.data.email,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))$""",
"""exa_json_path=$.data.username,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?))|({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
"""exa_json_path=$.data.userName,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?))|({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
"""exa_json_path=$.data.rulename,exa_field_name=alert_name""",
"""exa_json_path=$.data.dveventtype,exa_field_name=alert_type""",
"""exa_json_path=$.data.severity,exa_field_name=alert_severity""",
"""exa_json_path=$.data.sourceprocesscommandline,exa_field_name=process_command_line""",
"""exa_json_path=$.primaryDescription,exa_field_name=additional_info""",
"""exa_json_path=$.data.sourceprocessname,exa_field_name=process_name""",
"""exa_json_path=$.data.sourceprocessfilepath,exa_regex=^({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+))$""",
"""exa_json_path=$.data.sourceparentprocesspath,exa_field_name=parent_process_path""",
"""exa_json_path=$.data.alertid,exa_field_name=alert_id""",
"""exa_json_path=$.data.osType,exa_field_name=os""",
"""exa_json_path=$.activityType,exa_field_name=event_code""",
"""exa_json_path=$.accountId,exa_field_name=account_id""",
"""exa_json_path=$.accountName,exa_field_name=account_name""",
"""exa_json_path=$.data.srcport,exa_field_name=src_port""",
"""exa_json_path=$.data.dstport,exa_field_name=dest_port"""
]
ParserVersion = "v1.0.0"


}
```