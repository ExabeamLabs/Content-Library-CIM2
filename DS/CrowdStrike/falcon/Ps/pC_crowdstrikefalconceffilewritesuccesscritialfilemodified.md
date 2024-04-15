#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-file-write-success-critialfilemodified"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"CriticalFileModified""""
]
Fields = [
"""\"timestamp\":\"({time}\d{10})\""""
"""\"event_simpleName\":\"({event_code}[^\"]+)"""
"""\"aid\":\"({aid}[^\"]+)"""
"""\"TargetFileName\":\"({file_path}[^\"]+)"""
"""\"TargetFileName\":\"({file_dir}[^\"]*[\\\/]+)({file_name}[^\\\/\"]+)"""
"""({access}CriticalFileModified)"""
]
ParserVersion = "v1.0.0"


}
```