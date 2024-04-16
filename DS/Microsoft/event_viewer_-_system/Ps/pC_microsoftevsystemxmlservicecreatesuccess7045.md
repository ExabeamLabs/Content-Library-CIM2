#### Parser Content
```Java
{
Name = "microsoft-evsystem-xml-service-create-success-7045"
Vendor = "Microsoft"
Product = "Event Viewer - System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""">7045</EventID>"""
"""<Data Name""",
"""AccountName"""
]
Fields = [
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""ProcessID\\*=('|")({process_id}[^'"]+)"""
"""<Computer>({src_host}({host}[^<]+))</Computer>"""
 """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
""">({event_code}\d+)</EventID>"""
"""<Security UserID\\*=('|")({user_sid}[^"']+)"""
"""<Data Name\\*=('|")ServiceName('|")>({service_name}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")ServiceType('|")>({service_type}[^<]+?)\s*</Data>"""
"""<Data Name\\*=('|")ImagePath('|")>({process_path}({process_dir}[^<>\"]*?[\\\/]+)?({process_name}[^\"<>\\\/]*))</Data>"""
"""<Data Name\\*=('|")ImagePath('|")>({process_command_line}\"({process_path}({process_dir}[^<>\"]*?[\\\/]+)?({process_name}[^\"<>\\\/]*))\"(\s*({arg}[^<>]+))?)</Data>"""
"""<Data Name\\*=('|")AccountName('|")>(({account_domain}[^<>\\\/]+)[\\\/]+)?({account_name}[^<]+?)</Data>"""
"""({event_name}A service was installed in the system)""",
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```