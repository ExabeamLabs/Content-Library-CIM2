#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-activity-fdritemsexplorer
  ParserVersion = "v1.0.0"
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Conditions = [ """FalconGroupingTags""", """aid""", """"event_platform":""" ]
  Fields = [
    """"Time":"({time}\d{10})""",
    """"MD5HashData":\s*"({hash_md5}[A-Fa-f:\d.]+)""",
    """"ContextProcessId":\s*"({process_id}[^"]+)""",
    """"ParentProcessId":\s*"({parent_process_id}[^"]+)""",
    """"event_platform":\s*"({os}[^"]+)""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"name":\s*"({process_name}[^"]+)""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """"UserName":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|({user}[\w\.\-]{1,40}\$?)))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """CommandLine":"({process_command_line}.+?)","\w+":"""",
    """"RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"LocalPort":"({src_port}\d+)"""",
    """"RemotePort":"({dest_port}\d+)"""",
    """"aip":\s*"({aip}[A-Fa-f:\d.]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"UserSid":"({user_sid}[^"]+)"""",
    """"ComputerName":"({src_host}[^"]+)"""",
    """"City":"({location_city}[^"]+)"""",
    """"Version":"({os_version}[^"]+)"""",
    """"MachineDomain":"({domain}[^"]+)"""",
    """"UserPrincipal":\s*"(?:[^"@]+@)?({domain}[^"]+)""",
    """"Timezone":"({zone}[^"]+)"""",
    """"((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)""""
    """exa_json_path=$.Time,exa_regex=({time}\d{10})""",
    """exa_json_path=$.MD5HashData,exa_field_name=hash_md5""",
    """exa_json_path=$.ContextProcessId,exa_field_name=process_id""",
    """exa_json_path=$.ParentProcessId,exa_field_name=parent_process_id""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$.name,exa_field_name=process_name""",
    """exa_json_path=$.UserSid,exa_field_name=user_sid""",
    """exa_json_path=$.UserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?(?:SYSTEM|({user}[\w\.\-]{1,40}\$?)))""",
    """exa_json_path=$.src-account-name,exa_field_name=account_name""",
    """exa_json_path=$.CommandLine,exa_field_name=process_command_line""",
    """exa_regex=CommandLine":"({process_command_line}.+?)","\w+":"""",
    """exa_json_path=$.RemoteAddressIP4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.LocalPort,exa_field_name=src_port""",
    """exa_json_path=$.RemotePort,exa_field_name=dest_port""",
    """exa_json_path=$.aip,exa_field_name=aip""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.ComputerName,exa_field_name=src_host""",
    """exa_json_path=$.City,exa_field_name=location_city""",
    """exa_json_path=$.Version,exa_field_name=os_version""",
    """exa_json_path=$.MachineDomain,exa_field_name=domain""",
    """exa_json_path=$.UserPrincipal,exa_regex=(?:[^"@]+@)?({domain}[^"]+)""",
    """exa_json_path=$.Timezone,exa_field_name=zone""",
    """exa_regex="((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)""""
  ]


}
```