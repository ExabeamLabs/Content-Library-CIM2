#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-file-write-success-directorycreate"
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"""
""""DirectoryCreate""""
]
Fields = [
"""\"timestamp\":\s*\"({time}\d{10})"""
"""\"event_simpleName\":\s*\"({event_code}[^\"]+)"""
"""\"aid\":\s*\"({aid}[^\"]+)"""
"""\"TargetFileName\":\s*\"({file_path}[^\"]+)"""
""""TargetFileName":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?\s*({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\._\]\s]+)))?))"""",
"""({file_type}Directory)"""
"""suser=(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""src-account-name\":\"({account_name}[^\"]+)""",
""""aip":\s*"({aip}[^"]+)"""",
""""cid":"({cid}[^"]+)"""
""""event_platform":\s*"({os}[^"]+)""""
"""exa_json_path=$.timestamp,exa_field_name=time"""
"""exa_json_path=$.event_simpleName,exa_field_name=event_code"""
"""exa_json_path=$.aid,exa_field_name=aid"""
"""exa_regex="TargetFileName\":\s*\"({file_path}[^\"]+)"""
"""exa_regex="TargetFileName":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?\s*({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\._\]\s]+)))?))"""",
"""exa_regex=({file_type}Directory)"""
"""exa_regex="suser=(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""exa_json_path=$.src-account-name,exa_field_name=account_name"""
"""exa_json_path=$.aip,exa_field_name=aip"""
"""exa_json_path=$.cid,exa_field_name=cid"""
"""exa_json_path=$.event_platform,exa_field_name=os"""
]


}
```