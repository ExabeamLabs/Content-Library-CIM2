#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-create-success-processcreate"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""<Provider Name ='Microsoft-Windows-Sysmon'""",
"""<EventID>1</EventID>""",
"""<Channel>Microsoft-Windows-Sysmon/Operational</Channel>""",
"""<Data Name ="""
]
Fields = [
    """<Data Name ='UtcTime'>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)</Data>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({host}[^<]+?)</Computer>""",
    """<Data Name ='User'>((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\<]+?))\\)?(SYSTEM|(NETWORK|LOCAL) SERVICE|({user}[^<]+?))</Data>""",
    """<EventID>({event_code}\d+)""",
    """<Security UserID='({user_sid}[^>]+?)'/>""",
    """<Data Name ='LogonId'>({login_id}[^<]+?)</Data>""",
    """<Data Name ='Hashes'>[^=]*?MD5=({hash_md5}[A-F0-9a-f]+)[^<]*?<\/Data>""",
    """<Data Name ='ProcessGuid'>\{({process_guid}[A-F0-9a-f-]+)\}</Data>""",
    """<Data Name ='ProcessId'>({process_id}\d+)</Data>""",
    """<Data Name ='ParentProcessGuid'>\{({parent_process_guid}[A-F0-9a-f-]+)\}</Data>""",
    """<Data Name ='CommandLine'>"?\s*({process_command_line}[^<]+?)\s*</Data>""",
    """<Data Name ='Image'>(({process_dir}[^<]+)\\)?({process_name}[^<]+?)</Data>""",
    """<Data Name ='Image'>({process_path}[^<]+?)</Data>""",
    """<Data Name ='ParentImage'>({parent_process}(({parent_process_dir}[^<]+)\\)?({parent_process_name}[^<]+?))<\/Data>"""
]
DupFields = [ "host->src_host" ]
ParserVersion = "v1.0.0"


}
```