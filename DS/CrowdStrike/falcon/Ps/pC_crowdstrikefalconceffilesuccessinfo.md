#### Parser Content
```Java
{
Name = crowdstrike-falcon-cef-file-success-info
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"File"""
"""Info""""
]
ExtractionType = json
Fields = [
"""\"timestamp\":\s*\"*({time}\d{10})"""
"""\"UserIp\":\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WdestinationServiceName =({app}.+?)\s+\w+="""
""""destinationServiceName":"({app}.+?)"(\s+\w+=)?"""
"""\"event_simpleName\":\"({event_code}[^\"]+)"""
"""\"aid\":\"({aid}[^\"]+)"""
"""\"(ImageFileName|TargetFileName)\":\"({file_path}[^\"]+)"""
"""\"(ImageFileName|TargetFileName)\":\"({file_path}({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\-\.\_]{1,10}?)))?))\s*""""
"""\"SourceFileName\":\"({src_file_path}({src_file_dir}[^"]*[\\\/]+)({src_file_name}[^\\\/"]+?(\.(\d+|({src_file_ext}[^\\\/"\-\.\_]{1,10}?)))?))\s*""""
"""\"UserName\":\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
"""\"aip\":\"({aip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
"""\"ClientComputerName\":\"({src_host}[^\"]+)"""
"""\"id\":\"({alert_id}[\w-]+?)\""""
"""\"name\":\"({alert_name}[^\"]+?)\""""
"""\"File({operation}\w+)Info""""
""""cid":"({cid}[^"]+)"""
""""event_platform":"({os}[^"]+)"""",
""""FileSystemOperationType":"({operation_type}\d+)"""",
""""OciContainerId"\s*:\s*"({container_id}[^"]+)"""",
""""ShareAccess":"({access}[^"]+)"""",
"""exa_json_path=$..timestamp,exa_field_name=time""",
"""exa_json_path=$..destinationServiceName,exa_field_name=app"""
"""exa_json_path=$..event_simpleName,exa_field_name=event_code"""
"""exa_json_path=$..aid,exa_field_name=aid""",
"""exa_json_path=$..TargetFileName,exa_field_name=file_path"""
"""exa_regex="(ImageFileName|TargetFileName)\":\"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\-\.\_]{1,10}?)))?)\s*""""
"""exa_json_path=$..SourceFileName,exa_regex=({src_file_path}({src_file_dir}[^"]*[\\\/]+)({src_file_name}[^\\\/"]+?(\.(\d+|({src_file_ext}[^\\\/"\-\.\_]{1,10}?)))?))$"""
"""exa_json_path=$..aip,exa_field_name=aip""",
"""exa_json_path=$..id,exa_field_name=alert_id""",
"""exa_json_path=$..name,exa_field_name=alert_name""",
"""exa_regex="File({operation}\w+)Info"""",
"""exa_json_path=$..cid,exa_field_name=cid""",
"""exa_json_path=$..event_platform,exa_field_name=os""",
"""exa_json_path=$..OciContainerId,exa_field_name=container_id""",
"""exa_json_path=$..FileSystemOperationType,exa_field_name=operation_type""",
"""exa_json_path=$..ShareAccess,exa_field_name=access"""
]


}
```