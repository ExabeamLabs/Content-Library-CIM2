#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-alert-trigger-lsasshandlefromunsignedmodule
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"event_simpleName":""", """"LsassHandleFromUnsignedModule"""" ]
  Fields = [
    """"timestamp":\s*"({time}\d{10})""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"SourceFileName":\s*"({src_file_dir}[^"]+\\+)?({src_file_name}[^\\"]+)""",
    """"TargetFileName":\s*"({file_path}[^"]+)""",
    """"TargetFileName":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))""",
    """suser=(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """src-account-name":"({account_name}[^"]+)""",
    """"aip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"ConfigStateHash":\s*"({old_hash}[^"]+)""",
    """"SHA256HashData":\s*"({new_hash}[^"]+)""",
    """"ImageFileName":\s*"({file_path}[^"]+)""",
    """"ImageFileName":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?\.({file_ext}[^\\\.\s"]+)?)"""",
    """"ImageFileName\\*":\\*"({process_path}[^"]+\\({process_name}[^"\\]+))""",
# id is removed
    """"ContextProcessId":\s*"({process_guid}[^"]+)""",
# target_process_guid is removed
    """"name":\s*"({alert_name}[^",]+)"""",
    """"event_platform":\s*"({os}[^",]+)"""",
    """"cid":"({cid}[^"]+)"""
  ]
  DupFields = [
"alert_name->alert_subject"
]


}
```