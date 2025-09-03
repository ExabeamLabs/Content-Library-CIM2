#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-create-success-processcreate-1"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
Conditions = [
"""<Provider Name"""
"""Microsoft-Windows-Sysmon""",
"""<EventID>8</EventID>""",
"""<Channel>Microsoft-Windows-Sysmon/Operational</Channel>""",
"""<Data Name"""
]
Fields = [
    """<Data Name\\*=('|")UtcTime('|")>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)</Data>""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({src_host}({host}.+?))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data Name\\*=('|")User('|")>(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Security UserID\\*='({user_sid}.+?)'/>""",
    """<Data Name\\*=('|")Hashes('|")>.*?MD5=({hash_md5}[A-F0-9a-f]+).*?</Data>""",
    """(?i)<Data Name\\*=('|")SourceProcessGuid('|")>\{({process_guid}[A-F0-9a-f-]+)\}</Data>""",
    """<Data Name\\*=('|")SourceProcessId('|")>({process_id}\d+)</Data>""",
    """(?i)<Data Name\\*=('|")TargetProcessGuid('|")>\{({dest_process_id}[A-F0-9a-f-]+)\}</Data>""",
    """<Data Name\\*=('|")TargetProcessId('|")>({dest_process_id}\d+)</Data>""",
    """<Data Name\\*=('|")CommandLine('|")>({process_command_line}.+?)\s*</Data>""",
    """<Data Name\\*=('|")SourceImage('|")>({process_path}(({process_dir}[^<]*)\\+)?({process_name}.+?))</Data>""",
    """<Data Name\\*=('|")TargetImage('|")>({dest_process_path}(({dest_process_dir}[^<]*)\\+)?({dest_process_name}.+?))</Data>""",
    """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```