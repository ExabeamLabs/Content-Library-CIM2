#### Parser Content
```Java
{
Name = "microsoft-sysmon-kv-process-create-success-createremotethread"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Microsoft-Windows-Sysmon""",
"""CreateRemoteThread detected:"""
]
Fields = [
    """UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """Hostname":"({host}[^"]+?)"""",
    """\sComputer(?:Name)?\s*=\s*"?({host}[^\s"]+)""",
    """Message\s*=\s*"?({operation_type}[^:]+)""",
    """User\s*=\s*"(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """SourceProcessGuid:\s*\{({process_guid}[^\s\}]+)""",
    """SourceProcessId:\s*({process_id}\d+)""",
    """\s+SourceImage:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s+TargetProcessGuid:""",
    """TargetProcessGuid:\s*\{({dest_process_id}[^\s\}]+)""",
    """TargetProcessId:\s*({dest_process_id}\d+)""",
    """\s+TargetImage:\s*({dest_process_path}({dest_process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({dest_process_name}.+?))\s+NewThreadId:""",
    """EventID":({event_code}\d+),""",
    """"SourceImage":"({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+))"""",
    """"TargetImage":"({dest_process_path}(({dest_process_dir}[^"]*?)[\\\/]+)?({dest_process_name}[^"\\\/]+))"""",
    """AccountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """Domain":"({domain}[^"]+?)""""
]
DupFields = [  "host->src_host" ]
ParserVersion = "v1.0.0"


}
```