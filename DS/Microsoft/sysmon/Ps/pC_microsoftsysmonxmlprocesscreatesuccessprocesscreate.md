#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-create-success-processcreate"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
"""<Provider Name"""
"""Microsoft-Windows-Sysmon""",
"""<EventID>1</EventID>""",
"""<Channel>Microsoft-Windows-Sysmon/Operational</Channel>""",
"""<Data Name"""
]
Fields = [
    """<Data Name\\*=('|")UtcTime('|")>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)</Data>""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({src_host}({host}[^<]+?))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data Name\\*=('|")User('|")>((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\<]+?))\\)?(SYSTEM|(NETWORK|LOCAL) SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
    """<EventID>({event_code}\d+)""",
    """<Security UserID\\*=('|")({user_sid}[^>]+?)('|")/>""",
    """<Data Name\\*=('|")LogonId('|")>({login_id}[^<]+?)</Data>""",
    """<Data Name\\*=('|")Hashes('|")>[^=]*?MD5=({hash_md5}[A-F0-9a-f]+)[^<]*?<\/Data>""",
    """<Data Name\\*=('|")Hashes('|")>[^=]*?SHA256=({hash_sha256}[^<]+)<"""
    """<Data Name\\*=('|")ProcessGuid('|")>\{({process_guid}[A-F0-9a-f-]+)\}</Data>""",
    """<Data Name\\*=('|")ProcessId('|")>({process_id}\d+)</Data>""",
    """<Data Name\\*=('|")ParentProcessGuid('|")>\{({parent_process_guid}[A-F0-9a-f-]+)\}</Data>""",
    """<Data Name\\*=('|")ParentProcessId('|")>({parent_process_id}\d+)<"""
    """<Data Name\\*=('|")CommandLine('|")>"?\s*({process_command_line}[^<]+?)\s*</Data>""",
    """<Data Name\\*=('|")Image('|")>({process_path}(({process_dir}[^<]+?)[\\\/]+)?({process_name}[^\/\\<]+))<"""
    """<Data Name\\*=('|")Image('|")>(({process_dir}[^<]+)\\)?({process_name}[^<]+?)</Data>""",
    """<Data Name\\*=('|")Image('|")>({process_path}[^<]+?)</Data>""",
    """<Data Name\\*=('|")ParentImage('|")>({parent_process_path}(({parent_process_dir}[^<]+)\\)?({parent_process_name}[^<]+?))<\/Data>""",
    """<Data Name\\*=('|")ParentCommandLine('|")>({parent_process_command_line}[^<]+)<""",
    """<Data Name\\*=('|")ParentCommandLine('|")>({parent_process_command_line}[^<]+)<""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Execution.*?ThreadID=('|")({thread_id}\d+)""",
    """<Level>({run_level}[^<]+)<""",
    """<Data Name =('|")IntegrityLevel('|")>({process_integrity}[^<]+)<""",
    """<Data Name =('|")LogonId('|")>({login_id}[^<]+)<""",
    """<Data Name =('|")Description('|")>({additional_info}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```