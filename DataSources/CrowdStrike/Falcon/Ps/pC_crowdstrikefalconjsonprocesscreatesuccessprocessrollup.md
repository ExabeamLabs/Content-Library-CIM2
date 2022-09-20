#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-create-success-processrollup
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Conditions = [ 
""""event_simpleName":""""
"""ProcessRollup2""" 
]
  Fields = [
    """"aip":\s*"({host}[^"]+)""",
    """"aip":\s*"({dest_ip}[^"]+)"""
    """"timestamp":\s*"({time}\d{10})"""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"CommandLine":\s*"\s*({process_command_line}[^\n]+?)\s*"?,"""",
    """"CommandLine":\s*"\s*({process_path}({process_dir}[^,="]*?[\\\/]+)({process_name}[^\\\/=]*?))\s*",""",
    """"CommandLine":\s*"\s*[^",]*"({process_path}({process_dir}[^"=]*[\\\/]+?)({process_name}[^\\\/"=]+))""",
    """"CommandLine":\s*"\s*(?=[\\\/\w.]+\s+)(({process_dir}[^"=]*[\\\/]+?)({process_name}[^\s"=]+))""",
    """"CommandLine":\s*"\s*(?=[\w.]+\s+)({process_name}[^\s"=]+)""",
    """"CommandLine":\s*"\s*({process_path}({process_dir}[^,="-]*?[\\\/]+)({process_name}[^\\\/=]*?))(?:\s*-+\w+.*)"+,""",
    """"CommandLine":\s*"\s*(?=\w:[\\])({process_path}({process_dir}(?:[^"=]+)?[\\])?({process_name}[^\\\/"\s=]+))""",
    """"CommandLine":\s*"\s*(?=\\"*[^\\]*\\"*)\\"*({process_path}({process_dir}(?:[^"=]+)?[\\])?({process_name}[^\\\/"\s=]+))""",
    """"ImageFileName":\s*"({process_path}({process_dir}[^"]*?[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """"id":\s*"({process_guid}[^"]+)""",
    """"MD5HashData":\s*"({hash_md5}[^"]+)""",
    """"ParentProcessId":\s*"({parent_process_guid}[^"]+)""",
    """"TargetProcessId":\s*"({process_id}[^"]+)""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """log-severity\\=({log_severity}\S+)""",
    """src-account-name":"({account_name}[^"]+)""",
    """"((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)"""",
    """ParentBaseFileName":"({file_name}[^"]+)"""",
    """"ContextProcessId":"({process_guid}[^"]+)"""",
    """"ParentBaseFileName":"({parent_process}[^"]+)"""",
    """"GrandParentBaseFileName":"({grandparent_process_name}[^"]+)""""
  ]
 DupFields = [ "process_dir->process_path_directory", "parent_process_path->parent_process_path_name" ]


}
```