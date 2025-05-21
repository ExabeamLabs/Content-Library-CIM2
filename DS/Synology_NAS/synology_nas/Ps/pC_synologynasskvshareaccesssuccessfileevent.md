#### Parser Content
```Java
{
Name = "synologynas-s-kv-share-access-success-fileevent"
Vendor = "Synology NAS"
Product = "Synology NAS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
""" WinFileService Event:"""
""", File/Folder:"""
]
Fields = [
""">\w+ \d\d \d\d:\d\d:\d\d\s+({host}\S+)"""
"""Event:\s*({access}[^,]+),"""
"""Path:\s*({file_path}({file_dir}[^,]*?)[\\\/]*({file_name}[^,\\\/]+?)),"""
"""Path:\s*(?:[\\\/\*]+)?({share_name}[^\/]+)"""
"""File\/Folder:\s*({file_type}[^,]+?),"""
"""Size:\s*({bytes}[\d.]+)\s+({bytes_unit}\w+),"""
"""User:\s*(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?),"""
"""IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Source Port(=|:)\s*({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```