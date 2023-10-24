#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-create-success-processrollup
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Conditions = [ 
""""event_simpleName":""""
"""ProcessRollup2""" 
]
  Fields = [
    """"aip":\s*"({aip}[^"]+)""",
    """"aip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"timestamp":\s*"({time}\d{13})"""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"CommandLine":\s*"\s*({process_command_line}[^\n]+?)\s*"?,"""",
    """"ImageFileName":\s*"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """"MD5HashData":\s*"({hash_md5}[^"]+)""",
    """"ParentProcessId":\s*"({parent_process_id}[^"]+)""",
    """"TargetProcessId":\s*"({process_id}[^"]+)""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """log-severity\\=({log_severity}\S+)""",
    """src-account-name":"({account_name}[^"]+)""",
    """"((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)"""",
    """ParentBaseFileName":"({file_name}[^"]+)"""",
    """"ContextProcessId":"({process_guid}[^"]+)"""",
    """"ParentBaseFileName":"({parent_process}[^"]+)"""",
    """"GrandParentBaseFileName":"({grandparent_process_name}[^"]+)"""",
    """"event_platform":\s*"({os}[^"]+)"""
    """"IntegrityLevel":"({process_integrity}[^"]+)""""
    """"cid":"({cid}[^"]+)"""
    """\sUSER\\?=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?)(@({domain}[^"@]+?))?)(\s\w+\\?=|")"""
  ]
  DupFields = ["process_path->dest_process_path","process_dir->dest_process_dir","process_name->dest_process_name","process_command_line->dest_process_command_line"]


}
```