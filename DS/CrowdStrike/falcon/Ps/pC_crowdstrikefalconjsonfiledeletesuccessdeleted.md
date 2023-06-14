#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-file-delete-success-deleted
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"""
"""Deleted""""
]
Fields = [
""""timestamp":\s*"({time}\d{10})"""
""""event_simpleName":\s*"({event_code}[^\"]+)"""
""""aid":\s*"({aid}[^\"]+)"""
""""SourceFileName":\s*"({src_file_dir}[^\"]+\\+)?({src_file_name}[^\\\"]+)"""
""""TargetFileName":\s*"({file_path}[^\"]+)"""
""""TargetFileName":\s*"({file_dir}[^\"]*[\\\/]+)({file_name}[^\\\/\"]+?(\.({file_ext}[^\\\/\"\.]{1,10}?))?)\s*\""""
"""suser=(system|({user}[^\s]+))"""
"""src-account-name\":\"({account_name}[^\"]+)"""
""""((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^\"]+)""""
""""name":"({event_name}[^\"]+)\""""
"""UserName":"(({full_name}({first_name}[^\s\"]+)\s({last_name}[^\"]+))|({user}[^\"\s]+))""""
""""ContextProcessId":"({process_guid}[^\"]+)""""
""""aip":"({aip}[a-fA-F\d:.]+)""""
]


}
```