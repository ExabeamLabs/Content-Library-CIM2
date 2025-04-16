#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-process-create-success-1"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""<Provider Name"""
"""Microsoft-Windows-Sysmon"""
"""<EventID>1</EventID>"""
]
Fields = [
"""<Provider Name\\*='Microsoft-Windows-Sysmon' Guid='\{({process_guid}[^}]+?)\}"""
"""<EventID>({event_code}\d+)</EventID>"""
"""<Task>({operation}.*?)</Task>"""
"""<Execution ProcessID\\*='({process_id}\d+)"""
"""UtcTime:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
"""<Computer>({dest_host}({host}[\w\-.]+?))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<Security UserID\\*='(({domain}[^\\>]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s*/>"""
"""<EventData>.*?Image:\s*({process_path}({process_dir}.*?)({process_name}[^.\\]+\.exe))\s*CommandLine:"""
"""<EventData>.*?Image:\s*({path}.+?)\s*CommandLine:"""
"""CommandLine:\s*({process_command_line}.*?)\s*CurrentDirectory:"""
""",MD5=({hash_md5}[^,]+)(,|\s*$)"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```