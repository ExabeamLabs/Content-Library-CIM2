#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-file-success-567"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""Object Access Attempt"""
"""Image File Name:"""
]
Fields = [
"""({event_name}Object Access Attempt)"""
"""({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""(?i)(((audit|success)( |_)(success|audit))|information)\s*,\s*({dest_host}({host}[\w\-.]+))"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)"""
"""Audit\s*({dest_host}({host}[\w\-.]+?))\s+Object Access"""
"""User=(?:SYSTEM|NOT_TRANSLATED|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Sid="""
"""567\s*Security\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""({event_code}567)"""
"""Object Type:\s+({file_type}.+?)\s+Process ID:"""
"""Image File Name:\s+({src_file_path}.+?)\s+Accesses:"""
"""Accesses:\s+({access}.+?)\s+Access Mask:"""
"""Image File Name:\s*.*?\\?({src_file_name}([^\\]*?)({src_file_ext}\.[^\\]*?)?|[^\\]+)\s+Accesses:"""
"""Image File Name:\s*({file_dir}.+?)\\(?:[^\\]+?)\s+Accesses:"""
"""\s+Client Address:\s+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```