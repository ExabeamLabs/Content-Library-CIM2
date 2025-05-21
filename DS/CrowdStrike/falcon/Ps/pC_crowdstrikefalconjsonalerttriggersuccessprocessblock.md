#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-alert-trigger-success-processblock
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  ParserVersion = v1.0.0
  TimeFormat = ["epoch", "epoch_sec"]
  Conditions = [ """"event_simpleName":"ProcessBlocked"""", """"aip"""", """"aid"""" ]
  Fields = [
    """timestamp":"({time}\d{10,13})"""
    """"event_simpleName":"({event_name}[^"]+)"""",
    """"aip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"event_platform":"({os}[^"]+)"""",
    """"UserSid":"({user_sid}[^"]+)"""",
    """"ParentBaseFileName":"({parent_process_name}[^"]+)"""",
    """"MD5HashData":"({hash_md5}[^"]+)"""",
    """"CommandLine":"({process_command_line}.+?"),"\w+":"""",
    """"TargetProcessId":"({process_id}\d+)"""",
    """"ImageFileName":"({process_path}[^"]+(\/|\\)({process_name}[^"\\]+))""""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_name""",
    """exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.UserSid,exa_field_name=user_sid""",
    """exa_json_path=$.ParentBaseFileName,exa_field_name=parent_process_name""",
    """exa_json_path=$.MD5HashData,exa_field_name=hash_md5""",
    """exa_json_path=$.CommandLine,exa_field_name=process_command_line""",
    """exa_json_path=$.TargetProcessId,exa_field_name=process_id""",
    """exa_json_path=$.ImageFileName,exa_regex=({process_path}[^"]+(\/|\\)({process_name}[^"\\]+))"""
  ]


}
```