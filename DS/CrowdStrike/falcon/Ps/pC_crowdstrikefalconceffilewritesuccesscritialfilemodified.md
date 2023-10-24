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
"""\"timestamp\":\"({time}\d{10})"""
"""\"event_simpleName\":\"({event_code}[^\"]+)"""
"""\"aid\":\"({aid}[^\"]+)"""
"""\"TargetFileName\":"({file_path}(({file_dir}[^"]+)[\\\/]+)?(({file_name}[^"\\\/]+?(\.({file_ext}[^\."]+))?)))""""
"""\"TargetFileName\":\"({file_dir}[^\"]*[\\\/]+)({file_name}[^\\\/\"]+)"""
""""cid":"({cid}[^"]+)"""
"""({operation}CriticalFileModified)"""
""""event_platform":"({os}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```