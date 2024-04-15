#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-file-write-success-directorycreate"
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"""
""""DirectoryCreate""""
]
Fields = [
"""\"timestamp\":\s*\"({time}\d{10})\""""
"""\"event_simpleName\":\s*\"({event_code}[^\"]+)"""
"""\"aid\":\s*\"({aid}[^\"]+)"""
"""\"TargetFileName\":\s*\"({file_path}[^\"]+)"""
"""\"TargetFileName\":\s*\"({file_dir}[^\"]*[\\\/]+)({file_name}[^\\\/\"]+)"""
"""({file_type}Directory)"""
"""suser=(system|({user}[^\s]+))"""
"""src-account-name\":\"({account_name}[^\"]+)"""
]


}
```