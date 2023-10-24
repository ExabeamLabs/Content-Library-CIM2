#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-app-activity-eventsimplename-1
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_simpleName":""" , """"aip":""", """aid":""" ]
  Fields = ${DLCrowdStrikeParserTemplates.crowdstrike-process-info.Fields}[
    """"aip":\s*"({aip}[A-Fa-f:\d.]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"UserSid":"({user_sid}[^"]+)"""",
    """"UserPrincipal":\s*"(?:[^"@]+@)?({domain}[^"]+)""",
    """"UserPrincipal":"({user}[\w\.\-]{1,40}\$?)@({domain}[^"]+)""""
    """"((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)""""
    """"ClientComputerName":\s*"({src_host}[^"]+)"""
    """"cid":"({cid}[^"]+)"""
  ]
  DupFields = ["aip->src_ip"]

crowdstrike-process-info = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Fields = [
    """"timestamp":\s*"({time}\d{13})""",
    """"MD5HashData":\s*"({hash_md5}[A-Fa-f:\d.]+)""",
    """"ContextProcessId":\s*"({process_id}[^"]+)""",
    """"ParentProcessId":\s*"({parent_process_id}[^"]+)""",
    """"event_platform":\s*"({os}[^"]+)""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"name":\s*"({process_name}[^"]+)""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """"UserName":\s*"(?:(?:NT AUTHORITY|({domain}[^\\",]+?))\\+)?\s*(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """CommandLine":"({process_command_line}.+?)","\w+":"""",
    """"RemoteAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"LocalPort":"({src_port}\d+)"""",
    """"RemotePort":"({dest_port}\d+)"""",
    """"aid":"({aid}[^"]+)"""",
    """"aip":"({aip}[^"]+)""""
  
}
```