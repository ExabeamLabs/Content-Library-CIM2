#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-file-read-success-ransomware"
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"RansomwareOpenFile""""
""""timestamp":""""
]
Fields = [
"""\"timestamp\":\"({time}\d{10})"""
"""requestClientApplication=({app}[^=]+?)\s*\w+="""
"""\"aip\":\"({aip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
"""\"event_simpleName\":\"({event_code}[^\"]+)\""""
"""\"TargetFileName\":\"({file_dir}[^\"]*[\\\/]+)\s*({file_name}[^\\\/\"]+(\.({file_ext}[^\\\/\"]+)))\""""
"""\"TargetFileName\":\"({file_path}[^\"]+)\""""
"""\"FileObject\":\"({object}[^\"]+)\""""
"""\"aid\":\"({aid}[^\"]+)\""""
""""ShareAccess":"({access}[^"]+)""""
""""cid":"({cid}[^"]+)"""
""""event_platform":"({os}[^"]+)""""
]


}
```