#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-scheduled-task-create-success-win"
Conditions = [
""""event_simpleName":"ScheduledTaskRegistered"""
""""event_platform":"Win""""
]
ParserVersion = "v1.0.0"

crowdstrike-file-operations.Fields}[
"""\"+aip\"+:\"+({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""DownloadPort\"+:\"+({dest_port}\d+)"""
"""DownloadServer\"+:\"+({dest_host}[^\"]+)"""
"""\"ConfigStateHash\":\"({old_hash}[^\"]+)"""
"""\"SHA256HashData\":\"({new_hash}[^\"]+)"""
""""timestamp":\s*"({time}\d{13})"""",
""""DownloadPath":"({file_url}({src_file_path}(({file_dir}[^"]+)[\\\/]+)?(({src_file_name}[^"\\\/]+?(\.({src_file_ext}[^\."]+))?))))"""",
""""TargetFileName":"({file_path}(({file_dir}[^"]+)[\\\/]+)?(({file_name}[^"\\\/]+?(\.({file_ext}[^\."]+))?)))"""",
""""cid":"({cid}[^"]+)"""
"""exa_json_path=$.aip,exa_regex=({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.DownloadPort,exa_field_name=dest_port""",
"""exa_json_path=$.DownloadServer,exa_field_name=dest_host""",
"""exa_json_path=$.ConfigStateHash,exa_field_name=old_hash""",
"""exa_json_path=$.SHA256HashData,exa_field_name=new_hash""",
"""exa_regex="DownloadPath":"({file_url}({src_file_path}(({file_dir}[^"]+)[\\\/]+)?(({src_file_name}[^"\\\/]+?(\.({src_file_ext}[^\."]+))?))))"""",
"""exa_regex="TargetFileName":"({file_path}(({file_dir}[^"]+)[\\\/]+)?(({file_name}[^"\\\/]+?(\.({file_ext}[^\."]+))?)))"""",
"""exa_json_path=$.cid,exa_field_name=cid"""

}
```