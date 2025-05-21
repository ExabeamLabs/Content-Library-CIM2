#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-create-success-processrollup
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = ["epoch", "epoch_sec"]
  Conditions = [ 
""""event_simpleName":""""
"""ProcessRollup2""" 
]
  Fields = [
    """"OciContainerId"\s*:\s*"({container_id}[^"]+)"""",
    """"aip":\s*"({aip}[^"]+)""",
    """"aip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""" #Endpoints are monitored and managed by deploying a single lightweight sensor. The aip is the sensor's public IP, which can be used to pinpoint a computer's location depending on your network. Hence, in all CrowdStrike parsers, it is parsed as src_ip.
    """"ProcessStartTime":\s*"({time}\d{10,13})""",
    """"timestamp":\s*"({time}\d{10,13})"""",
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
    """"(SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)"""",
    """ParentBaseFileName":"({file_name}[^"]+)"""",
    """"ContextProcessId":"({process_guid}[^"]+)"""",
    """"ParentBaseFileName":"({parent_process_name}[^"]+)"""",
    """"GrandParentBaseFileName":"({grandparent_process_name}[^"]+)"""",
    """"event_platform":\s*"({os}[^"]+)"""
    """"IntegrityLevel":"({process_integrity}[^"]+)""""
    """"cid":"({cid}[^"]+)"""
    """"Desktop":"({client}[^",]+)"""
    """"SourceThreadId":"({thread_id}[^",]+)"""
    """"name":"({event_name}[^",]+)"""
    """\sUSER\\?=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"@]+?))?)(\s\w+\\?=|")"""
    """"GID":"({group_id}[^"]+)""""
    """'Content-Type:({web_content_type}[^']+)'"""
    """exa_json_path=$.OciContainerId,exa_field_name=container_id""",
    """exa_json_path=$..aip,exa_field_name=aip""",
    """exa_json_path=$..aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..timestamp,exa_field_name=time""",
    """exa_json_path=$.raw-event.timestamp,exa_field_name=time""",
    """exa_json_path=$..event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$..aid,exa_field_name=aid""",
    """exa_json_path=$..CommandLine,exa_field_name=process_command_line""",
    """exa_regex="ImageFileName":\s*"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """exa_json_path=$..MD5HashData,exa_field_name=hash_md5""",
    """exa_json_path=$..ParentProcessId,exa_field_name=parent_process_id""",
    """exa_json_path=$..TargetProcessId,exa_field_name=process_id""",
    """exa_json_path=$..UserSid,exa_field_name=user_sid""",
    """exa_regex=log-severity\\=({log_severity}\S+)""",
    """exa_json_path=$.src-account-name,exa_field_name=account_name""",
    """exa_json_path=$..SHA256String,exa_field_name=hash_sha256"""
    """exa_json_path=$..SHA256HashData,exa_field_name=hash_sha256"""",
    """exa_json_path=$..ParentBaseFileName,exa_field_name=file_name""",
    """exa_json_path=$..ContextProcessId,exa_field_name=process_guid""",
    """exa_json_path=$..ParentBaseFileName,exa_field_name=parent_process_name""",
    """exa_json_path=$..GrandParentBaseFileName,exa_field_name=grandparent_process_name""",
    """exa_json_path=$..event_platform,exa_field_name=os""",
    """exa_json_path=$..event_platform,exa_field_name=os""",
    """exa_json_path=$..IntegrityLevel,exa_field_name=process_integrity""",
    """exa_json_path=$..cid,exa_field_name=cid""",
    """exa_regex=\sUSER\\?=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"@]+?))?)(\s\w+\\?=|")"""
    """exa_json_path=$..Desktop,exa_field_name=client""",
    """exa_json_path=$..SourceThreadId,exa_field_name=thread_id""",
    """exa_json_path=$..name,exa_field_name=event_name""",
    """exa_json_path=$..GID,exa_field_name=group_id"""
    """exa_regex='Content-Type:({web_content_type}[^']+)'"""
  ]
  DupFields = ["process_path->dest_process_path","process_dir->dest_process_dir","process_name->dest_process_name","process_command_line->dest_process_command_line"]


}
```