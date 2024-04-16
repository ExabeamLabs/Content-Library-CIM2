#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-file-read-success-ransomware"
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
ExtractionType = json
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
""""cid":"({cid}[^"]+)"""
""""event_platform":\s*"({os}[^"]+)""""
"""exa_json_path=$.timestamp,exa_field_name=time"""
"""exa_regex=requestClientApplication=({app}[^=]+?)\s*\w+="""
"""exa_json_path=$.aip,exa_field_name=aip"""
"""exa_json_path=$.event_simpleName,exa_field_name=event_code"""
"""exa_regex="TargetFileName\":\"({file_dir}[^\"]*[\\\/]+)\s*({file_name}[^\\\/\"]+(\.({file_ext}[^\\\/\"]+)))\""""
"""exa_regex="TargetFileName\":\"({file_path}[^\"]+)\""""
"""exa_json_path=$.FileObject,exa_field_name=object"""
"""exa_json_path=$.aid,exa_field_name=aid"""
"""exa_json_path=$.cid,exa_field_name=cid"""
"""exa_json_path=$.event_platform,exa_field_name=os"""
]


}
```