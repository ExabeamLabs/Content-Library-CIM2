#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-file-download-success-bitsjobcreated
    ParserVersion = "v1.0.0"
    Conditions = [
""""event_simpleName":"BITSJobCreated""""
]
  
crowdstrike-file-operations = {
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Fields = [
"""\"timestamp\":\s*\"({time}\d{10})\""""
"""\"event_simpleName\":\s*\"({event_code}[^\"]+)"""
"""\"aid\":\s*\"({aid}[^\"]+)"""
"""\"SourceFileName\":\s*\"({src_file_dir}[^\"]+\\+)?({src_file_name}[^\\\"]+)"""
"""\"TargetFileName\":\s*\"({src_file_path}[^\"]+)"""
""""TargetFileName":\s*"({file_dir}[^"]*[\\\/]+)({src_file_name}[^\\\/"]+?(\.(\d+|({src_file_ext}[^\\\/"\.]+?)))?)\s*""""
"""suser=(system|({user}[^\s]+))"""
"""src-account-name\":\"({account_name}[^\"]+)"""
"""\"((?i)SHA256String|SHA256HashData)\":\"({hash_sha256}[^\"]+)\""""
"""\"name\":\"({event_name}[^\"]+)\""""
"""UserName\":\"(({full_name}({first_name}[^\s\"]+)\s({last_name}[^\"]+))|({user}[^\"\s]+))\""""
"""\"ContextProcessId\":\"({process_guid}[^\"]+)\""""
""""aip":"({src_ip}[a-fA-F\d:.]+)""""
""""Size":"({bytes}\d+)""""

}
```