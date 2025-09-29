#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-file-write-success-critialfilemodified"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
ExtractionType = json
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
""""LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""ComputerName":"({host}[\w\-\.]+)""""
""""aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""exa_json_path=$.timestamp,exa_field_name=time""",
"""exa_json_path=$.event_simpleName,exa_field_name=event_code""",
"""exa_json_path=$.aid,exa_field_name=aid""",
"""exa_regex="TargetFileName\":"({file_path}(({file_dir}[^"]+)[\\\/]+)?(({file_name}[^"\\\/]+?(\.({file_ext}[^\."]+))?)))""""
"""exa_regex="TargetFileName\":\"({file_dir}[^\"]*[\\\/]+)({file_name}[^\\\/\"]+)"""
"""exa_json_path=$.cid,exa_field_name=cid""",
"""exa_regex=({operation}CriticalFileModified)"""
"""exa_json_path=$.event_platform,exa_field_name=os"""
"""exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)"""
"""exa_json_path=$.aip,exa_field_name=aip"""
]
ParserVersion = "v1.0.0"


}
```