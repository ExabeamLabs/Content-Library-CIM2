#### Parser Content
```Java
{
Name = "microsoft-sysmon-json-process-create-success-processcreate"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Microsoft-Windows-Sysmon""",
"""Process Create:""",
""""AccountName":""""
]
Fields = [
    """"UtcTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"Image":"({process_path}(({process_dir}[^"]+?)[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """"TargetFilename":"({dest_process_path}(({dest_process_dir}[^"]+?)[\\\/]+)?({dest_process_name}[^"\\\/]+?(\.({file_ext}\w+))?))"""",
    """"Domain":"(NT AUTHORITY|({domain}[^"]+))""",
    """"AccountName":"(SYSTEM|({user}[\w\.\-]{1,40}\$?))""",
    """"ProcessID":({process_id}\d+)""",
    """"ProcessGuid":"({process_guid}[^"]+)""",
    """"ParentProcessGuid":"({parent_process_guid}[^"]+)""",
    """"LogonId":"({login_id}[^"]+)""",
    """"Hashes":"[^]]+MD5=({hash_md5}[^,\s]+),""",
    """"Hostname":"({host}[^"]+)""",
    """"CommandLine":"\s*({process_command_line}[^,]+?)\s*",""",
    """"ParentImage":"({parent_process}(({parent_process_dir}[^"]+?)[\\\/]+)?({parent_process_name}[^"\\\/]+))"""",
    """"EventID":({event_code}\d+)""",
    """ProviderGuid":"({provider_guid}[^"]+)""",
    """"Task":({task}\d+)""",
    """"OpcodeValue":({opcode_value}\d+)""",
    """"User":"(((?i)NT AUTHORITY|({domain}[^\\]+))[\\]+)?((?i)SYSTEM|LOCAL SERVICE|NETWORK SERVICE|({user}[\w\.\-]{1,40}\$?))"""",
    """"LogonGuid":"({logon_guid}[^"]+)""",
    """"Hashes":"[^]]+SHA256=({hash_sha256}[^",]+)""",
    """"ParentCommandLine":"\s*({parent_process_command_line}[^,]+?)\s*",""",
]
DupFields = [ "host->src_host" ]
ParserVersion = "v1.0.0"


}
```