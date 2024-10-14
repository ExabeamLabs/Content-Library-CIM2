#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-file-write-success-11-1"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""<Provider Name"""
"""<Channel>Microsoft-Windows-Sysmon"""
"""logrhythm:"""
"""<EventID>11</EventID>"""
]
Fields = [
"""<Provider Name\\*='Microsoft-Windows-Sysmon' Guid='\{({process_guid}[^}]+?)\}"""
"""<EventID>({event_code}\d+)</EventID>"""
"""<Task>({operation}.*?)</Task>"""
"""<Execution ProcessID\\*='({process_id}\d+)"""
"""created:UtcTime:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
"""<Computer>({dest_host}({host}[\w\-.]+?))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<Security UserID\\*='(({domain}[^\\>]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s*/>"""
"""<EventData>.*?Image:\s*({process_path}({process_dir}.*?)({process_name}[^.\\]+\.exe))\s*TargetFilename:"""
"""<EventData>.*?Image:\s*({path}.+?)\s*TargetFilename:"""
"""TargetFilename:\s*({file_path}({file_dir}.*?)({file_name}[^\\.]+(\.({file_ext}[^\\.]+?))?))\s*CreationUtcTime:"""
]
ParserVersion = "v1.0.0"


}
```