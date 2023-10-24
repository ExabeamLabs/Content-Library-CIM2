#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-activity-fdritemsexplorer
  ParserVersion = "v1.0.0"
  Vendor = CrowdStrike
  Product = Falcon
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
  ]


}
```