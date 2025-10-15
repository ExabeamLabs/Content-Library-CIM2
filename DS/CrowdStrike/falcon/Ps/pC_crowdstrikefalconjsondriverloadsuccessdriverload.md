#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-driver-load-success-driverload
    Conditions = [ """"event_simpleName":"DriverLoad"""" ]
    ParserVersion = "v1.0.0"
    ExtractionType = json
  
crowdstrike-process-info-1 = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = ["epoch", "epoch_sec"]
  Fields = [
    """"timestamp":\s*"({time}\d{10,13})""",
    """"ContextProcessId":\s*"({process_id}[^"]+)""",
    """"ContextBaseFileName":"({file_name}[^"]+)""""
    """"ParentProcessId":\s*"({parent_process_id}[^"]+)""",
    """"event_platform":\s*"({os}[^"]+)""",
    """"name":\s*"({event_code}({event_name}[^"]+))""",    #These changes are done as a part of NGCIM-6070. The value in this field is not actual process_name and it is event_name instead.
    """"event_simpleName":\s*"({event_code}({event_name}[^"]+))""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """"UserName":\s*"(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """CommandLine":"({process_command_line}.+?)","\w+":"""",
    """"RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"LocalPort":"({src_port}\d+)"""",
    """"RemotePort":"({dest_port}\d+)"""",
    """"ConfigStateHash\\*"+:\\*"+({old_hash}[^\\"]+)""",
    """"aid":"({aid}[^"]+)"""",
    """"aip\\*"+:\\*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"MD5HashData":\s*"({hash_md5}[A-Fa-f:\d.]+)""",
    """"SHA256HashData\\*"+:\\*"+({hash_sha256}[^"\\]+)""",
    """"TargetProcessId\\*"+:\\*"+({process_id}[^"\\]+)""",
    """"(ImageFileName|TargetFileName)\\*"+:\\*"+(({file_path}[^"]+?))\\*"""",
    """"(ImageFileName|TargetFileName)\\*"+:\\*"+({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.ContextProcessId,exa_field_name=process_id""",
    """exa_json_path=$.ParentProcessId,exa_field_name=parent_process_id""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.name,exa_field_name=event_name""",
    """exa_json_path=$.name,exa_field_name=event_code""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_name""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$.UserSid,exa_field_name=user_sid""",
    """exa_json_path=$.UserName,exa_regex=(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_regex=rc-account-name":"({account_name}[^"]+)""",
    """exa_json_path=$.CommandLine,exa_field_name=process_command_line""",
    """exa_regex="RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """exa_regex="LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex="LocalPort":"({src_port}\d+)"""",
    """exa_regex="RemotePort":"({dest_port}\d+)"""",
    """exa_json_path=$.ConfigStateHash,exa_field_name=old_hash""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_regex="MD5HashData":\s*"({hash_md5}[A-Fa-f:\d.]+)""",
    """exa_regex="SHA256HashData\\*"+:\\*"+({hash_sha256}[^"\\]+)""",
    """exa_regex="TargetProcessId\\*"+:\\*"+({process_id}[^"\\]+)""",
    """exa_json_path=$.MD5HashData,exa_field_name=hash_md5""",
    """exa_json_path=$.SHA256HashData,exa_field_name=hash_sha256""",
    """exa_json_path=$.TargetProcessId,exa_field_name=process_id""",
    """exa_regex="(ImageFileName|TargetFileName)\\*"+:\\*"+(({file_path}[^"]+?))\\*"""",
    """exa_regex="(ImageFileName|TargetFileName)\\*"+:\\*"+({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """exa_json_path=$.ContextBaseFileName,exa_field_name=file_name"""
    """exa_regex="TargetImageFileName":\s*"[\\\?]*(|({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+?))?))""""
  
}
```