#### Parser Content
```Java
{
Name = "microsoft-sysmon-kv-process-create-success-processcreate-1"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
Conditions = [
"""Process Create: """,
""" ProcessGuid: """,
""" ParentProcessGuid: """
]
Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}[\w\-.]+)\s""",
    """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\sComputer="({host}[\w\-.]+)"""",
    """User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """Domain=({domain}.+?)\s+(\w+=|$)""",
    """User:\s*(?:(NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\]+))\\)?(SYSTEM|(NETWORK|LOCAL) SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+LogonGuid:""",
    """Sid=\s*({user_sid}[^\s]+)""",
    """LogonId:\s*({login_id}[^\s]+)""",
    """Hashes:\s*,?MD5=({hash_md5}[^\s,]+)""",
    """({event_name}Process Create)""",
    """\sProcessGuid:\s*\{({process_guid}[^\s\}]+)""",
    """\sProcessId:\s*({process_id}\d+)""",
    """ParentProcessGuid:\s*\{({parent_process_guid}[^\s\}]+)""",
    """CommandLine:\s*"*({process_command_line}.+?)\s*"*\s*CurrentDirectory:""",
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^:]+?))\s+(\w+:|$)""",
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^:]+?))\s+CommandLine:""",
    """\s+Image:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^:]+?))\s+FileVersion:""",
    """\s+ParentImage:\s*({parent_process_path}({parent_process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({parent_process_name}[^:]+?))\s+ParentCommandLine:"""
    """IntegrityLevel:\s*({process_integrity}[^\s]+)"""
]
DupFields = [   "host->src_host" ]
ParserVersion = "v1.0.0"


}
```