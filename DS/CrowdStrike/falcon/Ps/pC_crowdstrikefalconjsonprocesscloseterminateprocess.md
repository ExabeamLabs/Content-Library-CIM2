#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-close-terminateprocess
  ExtractionType = json
  ParserVersion = v1.0.0
  Conditions = [ """"event_simpleName":"TerminateProcess"""" ]

crowdstrike-process-info = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = ["epoch_sec","epoch"]
  Fields = [
    """"timestamp":\s*"({time}\d{10,13})""",
    """"MD5HashData":\s*"({hash_md5}[A-Fa-f:\d.]+)""",
    """"ContextProcessId":\s*"({process_id}[^"]+)""",
    """"ParentProcessId":\s*"({parent_process_id}[^"]+)""",
    """"event_platform":\s*"({os}[^"]+)""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """"UserName":\s*"(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """CommandLine":"({process_command_line}[^"]+?)\s*"""",
    """"RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"LocalPort":"({src_port}\d+)"""",
    """"RemotePort":"({dest_port}\d+)"""",
    """"aid":"({aid}[^"]+)"""",
    """"aip":"({aip}[^"]+)"""",
    """"OciContainerId"\s*:\s*"({container_id}[^"]+)"""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.MD5HashData,exa_field_name=hash_md5""",
    """exa_json_path=$.ContextProcessId,exa_field_name=process_id""",
    """exa_json_path=$.ParentProcessId,exa_field_name=parent_process_id""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$.UserSid,exa_field_name=user_sid""",
    """exa_json_path=$.UserName,exa_regex=(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_regex=src-account-name":"({account_name}[^"]+)""",
    """exa_json_path=$.CommandLine,exa_field_name=process_command_line""",
    """exa_regex="RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """exa_regex="LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex="LocalPort":"({src_port}\d+)"""",
    """exa_regex="RemotePort":"({dest_port}\d+)"""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.aip,exa_field_name=aip""",
    """exa_json_path=$.cid,exa_field_name=cid""",
    """exa_json_path=$.OciContainerId,exa_field_name=container_id"""
  
}
```