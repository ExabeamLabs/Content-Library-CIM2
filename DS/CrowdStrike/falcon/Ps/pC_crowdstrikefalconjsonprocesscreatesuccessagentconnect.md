#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-create-success-agentconnect
  Conditions = [ """"event_simpleName":"AgentConnect"""", """"destinationServiceName":"CrowdStrike"""" ]
  ParserVersion = "v1.0.0"

crowdstrike-process-info-1 = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Fields = [
    """"timestamp":\s*"({time}\d{13})""",
    """"ContextProcessId":\s*"({process_id}[^"]+)""",
    """"ParentProcessId":\s*"({parent_process_id}[^"]+)""",
    """"event_platform":\s*"({os}[^"]+)""",
    """"event_simpleName":\s*"({event_name}[^"]+)""",
    """"name":\s*"({process_name}[^"]+)""",
    """"id":\s*"({user_sid}[^"]+)""",
    """"UserName":\s*"(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|({user}[^",]+))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """CommandLine":"({process_command_line}.+?)","\w+":"""",
    """"RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"LocalPort":"({src_port}\d+)"""",
    """"RemotePort":"({dest_port}\d+)"""",
    """"ConfigStateHash\\*"+:\\*"+({old_hash}[^\\"]+)""",
    """"aid":"({aid}[^"]+)"""",
    """"aip\\*"+:\\*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"MD5HashData":\s*"({hash_md5}[A-Fa-f:\d.]+)""",
    """"SHA256HashData\\*"+:\\*"+({hash_sha256}[^"\\]+)""",
    """"TargetProcessId\\*"+:\\*"+({process_id}[^"\\]+)""",
    """"(ImageFileName|TargetFileName)\\*"+:\\*"+(({file_path}[^"]+?))\\*"""",
    """"(ImageFileName|TargetFileName)\\*"+:\\*"+({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
  ]
  DupFields = ["event_name->event_code"
}
```