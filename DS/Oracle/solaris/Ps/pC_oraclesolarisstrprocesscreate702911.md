#### Parser Content
```Java
{
Name = "oracle-solaris-str-process-create-702911"
Vendor = "Oracle"
Product = "Solaris"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""from """
"""audit.notice"""
"""ID 702911"""
"""execve"""
]
Fields = [
"""({time}\d+-\d+-\d+\s\d+:\d+:\d+).[^,]+.[^,]+.({host}[^,]+)"""
"""({event_code}702911)\s({event_name}audit.notice)]\s*({operation}[^\s]+)"""
"""({result}(ok|failed))"""
"""session\s*({login_id}\d+)"""
"""by\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""as\s*({auth}[^\s]+)"""
"""\sin\s({src_zone}[^\s]+)"""
"""from\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""obj\s*(?:({process_path}({process_dir}[^\s]*?)(\/+({process_name}[^\/]+?))?))\s+"""
"""argv\s*({process_command_line}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```