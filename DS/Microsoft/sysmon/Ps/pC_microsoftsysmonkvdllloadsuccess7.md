#### Parser Content
```Java
{
Name = "microsoft-sysmon-kv-dll-load-success-7"
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""Event ID: 7"""
"""Image loaded:"""
"""ProviderName: Microsoft-Windows-Sysmon"""
]
Fields = [
"""Event ID:\s*({event_code}\d+)"""
"""ComputerName(:|=)\s*({host}[\w.-]+)"""
"""UtcTime:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
"""User:\s*({user}[\w\.\-]{1,40}\$?)\s*\w+:"""
"""ProcessGuid:\s*\{({process_guid}[^}]+?)\}"""
"""ProcessId:\s*({process_id}\d+)"""
"""Image:\s*({process_path}({process_dir}(\w+:)?[^:]+\\)({process_name}[^\\]+\.exe))\s*\w+:"""
"""Image:\s*({path}.+?)\s*\w+:"""
"""ImageLoaded:\s*({file_path}({file_dir}(\w+:)?[^:]+\\)({file_name}[^\\.]+(\.({file_ext}[^\\.]+?))?))\s*\w+:"""
"""Hashes:\s*.*?MD5=({hash_md5}[A-F0-9a-f]+)"""
"""Hashes:\s*.*?SHA256=({hash_sha256}[A-F0-9a-f]+)"""
"""Hashes:\s*.*?IMPHASH=({imphash}[A-F0-9a-f]+)"""
"""Signed:\s*({signed}.+?)\s*\w+:"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```