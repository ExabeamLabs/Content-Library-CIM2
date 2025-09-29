#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-file-delete-success-deleted
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = "epoch"
Conditions = [
""""event_simpleName":"""
"""Deleted""""
]
Fields = [
""""timestamp":\s*"({time}\d{13})"""
""""event_simpleName":\s*"({event_code}[^\"]+)"""
""""aid":\s*"({aid}[^\"]+)"""
""""SourceFileName":\s*"({src_file_dir}[^\"]+\\+)?({src_file_name}[^\\\"]+)"""
""""TargetFileName":\s*"({file_path}[^\"]+)"""
""""TargetFileName":\s*"({file_dir}[^\"]*[\\\/]+)({file_name}[^\\\/\"]+?(\.({file_ext}[^\\\/\"\.]{1,10}?))?)\s*\""""
"""suser=(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""src-account-name\":\"({account_name}[^\"]+)"""
""""((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^\"]+)""""
""""name":"({event_name}[^\"]+)\""""
""""UserName":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
""""ContextProcessId":"({process_guid}[^\"]+)""""
""""aip":"({aip}[a-fA-F\d:.]+)""""
""""event_platform":"({os}[^"]+)""""
""""LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""ComputerName":"({host}[\w\-\.]+)""""
"""exa_json_path=$.timestamp,exa_field_name=time""",
"""exa_json_path=$.event_simpleName,exa_field_name=event_code""",
"""exa_json_path=$.aid,exa_field_name=aid""",
"""exa_json_path=$.SourceFileName,exa_regex=({src_file_dir}[^\"]+\\+)?({src_file_name}[^\\\"]+)""",
"""exa_json_path=$.TargetFileName,exa_field_name=file_path""",
"""exa_regex="TargetFileName":\s*"({file_dir}[^\"]*[\\\/]+)({file_name}[^\\\/\"]+?(\.({file_ext}[^\\\/\"\.]{1,10}?))?)\s*\""""
"""exa_regex="((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^\"]+)""""
"""exa_json_path=$.name,exa_field_name=event_name""",
"""exa_json_path=$.UserName,exa_regex=(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
"""exa_json_path=$.ContextProcessId,exa_field_name=process_guid""",
"""exa_json_path=$.aip,exa_regex=({aip}[a-fA-F\d:.]+)""",
"""exa_json_path=$.event_platform,exa_field_name=os"""
"""exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)"""
]


}
```