#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-activity-eventsimplename
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_simpleName":""" , """destinationServiceName =CrowdStrike""" ]
  Fields = ${DLCrowdStrikeParserTemplates.crowdstrike-process-info-2.Fields}[
    # entitlements is removed
    # effective_transmission_class is removed
    # config_state_hash is removed
    # config_build is removed
    # cid is removed
    """"aip":\s*"({aip}[A-Fa-f:\d.]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"UserSid":"({user_sid}[^"]+)"""",
    """"UserPrincipal":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)@([^"]+)""""
    """"(OriginalUserName|UserName)":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)""""
    """"event_platform":"({os}[^"]+)""""
    """"cid":"({cid}[^"]+)"""
  ]

crowdstrike-process-info-2 = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = ["epoch", "epoch_sec"]
  Fields = [
    """"timestamp":\s*"({time}\d{10,13})""",
    """"MD5HashData":\s*"({hash_md5}[A-Fa-f:\d.]+)""",
    """"ContextProcessId":\s*"({process_id}[^"]+)""",
    """"ParentProcessId":\s*"({parent_process_id}[^"]+)""",
    """"event_platform":\s*"({os}[^"]+)""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """"(OriginalUserName|UserName)":\s*"(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?\s*(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """"NewUsername":\s*"(?:SYSTEM|LOCAL SERVICE|-|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """CommandLine":"({process_command_line}.+?)","\w+":"""",
    """"RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"LocalPort":"({src_port}\d+)"""",
    """"RemotePort":"({dest_port}\d+)"""",
    """"aid":"({aid}[^"]+)"""",
    """"aip":"({aip}[^"]+)"""",
    """"QueryStatus":"({dns_query_flags}[^"]+)"""",
    """"ContextBaseFileName":"({file_name}[^"]+)""""
    """"timestamp":\s*"({time}\d{10})""",
    """"name":\s*"({event_name}[^"]+)"""
    """"(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.MD5HashData,exa_field_name=hash_md5""",
    """exa_json_path=$.ContextProcessId,exa_field_name=process_id""",
    """exa_json_path=$.ParentProcessId,exa_field_name=parent_process_id""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$.UserSid,exa_field_name=user_sid""",
    """exa_json_path=$.UserName,exa_regex=(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.OriginalUserName,exa_regex=(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.NewUsername,exa_regex=(?:SYSTEM|LOCAL SERVICE|-|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_regex=src-account-name":"({account_name}[^"]+)""",
    """exa_json_path=$.CommandLine,exa_field_name=process_command_line""",
    """exa_regex="RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """exa_regex="LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex="LocalPort":"({src_port}\d+)"""",
    """exa_regex="RemotePort":"({dest_port}\d+)"""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.aip,exa_field_name=aip"""
    """exa_json_path=$.QueryStatus,exa_field_name=dns_query_flags"""
    """exa_json_path=$.ContextBaseFileName,exa_field_name=file_name"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.name,exa_field_name=event_name"""
    """exa_regex="(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
    """exa_regex="(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
  
}
```