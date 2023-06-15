#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-close-terminateprocess
  ParserVersion = v1.0.0
  Conditions = [ """"event_simpleName":"TerminateProcess"""" ]

crowdstrike-process-info = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Fields = [
    """"timestamp":\s*"({time}\d{10})""",
    """"MD5HashData":\s*"({hash_md5}[A-Fa-f:\d.]+)""",
    """"ContextProcessId":\s*"({process_id}[^"]+)""",
    """"ParentProcessId":\s*"({parent_process_id}[^"]+)""",
    """"event_platform":\s*"({os}[^"]+)""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"name":\s*"({process_name}[^"]+)""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """"UserName":\s*"(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|({user}[^",]+))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """CommandLine":"({process_command_line}[^"]+?)\s*"""",
    """"RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"LocalPort":"({src_port}\d+)"""",
    """"RemotePort":"({dest_port}\d+)"""",
    """"aid":"({aid}[^"]+)"""",
    """"aip":"({aip}[^"]+)""""
  
}
```