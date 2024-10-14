#### Parser Content
```Java
{
Name = "microsoft-sysmon-kv-process-create-success-processcreate"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Microsoft-Windows-Sysmon""",
"""Process Create:""",
"""Event ID: 1"""
]
Fields = [
    """Hostname":"({host}[^"]+?)"""",
    """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\sComputer(?:Name)?\s*=\s*"?({host}[^\s"]+)""",
    """Message\s*=\s*"?({operation_type}[^:]+)""",
    """User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """Domain=({domain}.+?)\s+(\w+=|$)""",
    """User:\s*(?:({domain}[^\\]+)\\*)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+LogonGuid""",
    """Sid=\s*({user_sid}[^\s]+)""",
    """LogonId:\s*({login_id}[^\s]+)""",
    """Hashes:.*?,?MD5=({hash_md5}[^\s,]+)""",
    """ProcessGuid:\s*\{({process_guid}[^\s\}]+)""",
    """ProcessId:\s*({process_id}\d+)""",
    """ParentProcessGuid:\s*\{({parent_process_guid}[^\s\}]+)""",
    """CommandLine:\s*({process_command_line}.+?)\s*CurrentDirectory:""",
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s+CommandLine:""",
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s+FileVersion:""",
    """\s+ParentImage:\s*({parent_process_path}({parent_process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({parent_process_name}.+?))\s+ParentCommandLine:""",
    """ParentImage:\s*({parent_process_path}({parent_process_dir}.*?)({parent_process_name}[^.\\]+\.exe))\s*\w+:""",
    """ParentCommandLine:\s*\\?"({parent_process_command_line}.+?)\s+[^"]+""",
    """CommandLine:.*\s+config\s+({service_name}\S+)""",
    """binPath=\s*({service_command_line}(?:\"(.+)\")|(?:(\S+)))\s*CurrentDirectory:""",
    """CommandLine:.*\s+({parameter_sct}\S+\.sct)""",
    """CommandLine:.*\s+"({parameter_sct}.+\.sct)"""",
    """CommandLine:.*\s+({parameter_hta}\S+\.hta)""",
    """CommandLine:.*\s+"({parameter_hta}.+\.hta)"""",
    """CommandLine:.*\s+({parameter_xml}\S+\.xml)""",
    """CommandLine:.*\s+"({parameter_xml}.+\.xml)"""",
    """CommandLine:.*\s+({parameter_csproj}\S+\.csproj)""",
    """CommandLine:.*\s+"({parameter_csproj}.+\.csproj)"""",
    """CommandLine:.+?\/u\s*["\s]({parameter_exe}.+?\.exe)\s+CurrentDirectory:""",
    """CommandLine:.+?\/u\s*["\s]({parameter_dll}.+?\.dll)\s+CurrentDirectory:"""
    """IntegrityLevel:\s*({integrity}.+?)\s*\w+:""",
    """EventID":({event_code}\d+),""",
    """"Image":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """"ParentImage":"({parent_process_path}(({parent_process_dir}[^"]*?)[\\\/]+)?({parent_process_name}[^"\\\/]+))""""
]
DupFields = [  "host->src_host" ]
ParserVersion = "v1.0.0"


}
```