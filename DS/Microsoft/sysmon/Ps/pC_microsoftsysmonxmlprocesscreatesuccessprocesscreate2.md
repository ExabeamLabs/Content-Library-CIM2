#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-create-success-processcreate-2"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd HH:mm:ss.SSS"]
Conditions = [
"""<Provider Name"""
"""'Microsoft-Windows-Sysmon'""",
"""<EventID>10</EventID>""",
"""<Channel>Microsoft-Windows-Sysmon/Operational</Channel>""",
"""<Data Name"""
]
Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Data Name\\*='UtcTime'>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)</Data>""",
    """<Computer>({src_host}({host}({dest_host}[\w\-.]+)))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data Name\\*='User'>(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Security UserID\\*='({user_sid}[^']+)'/>""",
    """<Data Name\\*='Hashes'>.*?MD5=({hash_md5}[A-F0-9a-f]+).*?</Data>""",
    """(?i)<Data Name\\*='SourceProcessGuid'>\{({process_guid}[A-F0-9a-f-]+)\}</Data>""",
    """<Data Name\\*='SourceProcessId'>({process_id}\d+)</Data>""",
    """(?i)<Data Name\\*='TargetProcessGuid'>\{({dest_process_id}[A-F0-9a-f-]+)\}</Data>""",
    """<Data Name\\*='TargetProcessId'>({dest_process_id}\d+)</Data>""",
    """<Data Name\\*='CommandLine'>({process_command_line}[^<]+?)\s*</Data>""",
    """<Data Name\\*='SourceImage'>({parent_process_path}(({parent_process_dir}[^<]*)\\+)?({parent_process_name}[^<]+?))</Data>""",
    """<Data Name\\*='TargetImage'>({process_path}(({process_dir}[^<]*)\\+)?({process_name}[^<]+?))</Data>""",
    """<Data Name\\*='GrantedAccess'>({result}[^<]+)</Data>""",
    """<EventID>({event_code}\d+)""",
    """CallTrace:\s*({additional_info}[^<]+)</Message>"""
    """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```