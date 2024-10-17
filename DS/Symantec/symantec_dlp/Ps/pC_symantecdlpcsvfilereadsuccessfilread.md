#### Parser Content
```Java
{
Name = "symantec-dlp-csv-file-read-success-filread"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""",Rule:"""
""",File Read,Begin:"""
]
Fields = [
"""Begin:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
"""\w+ \d+ \d\d:\d\d:\d\d\s+({host}[\w\-.]+)"""
""",(0.0.0.0|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^,]*)),([^,]*,){2}File Read"""
"""Rule:[^\|]*\|\s*({operation_details}[^,]+)"""
"""User:\s*(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""Domain:\s*({domain}[^,]+)"""
""",File Read,([^,]*,){3}\d+,"?(?: |({process_path}({process_dir}(?:[^,"]+)?[\\\/])?({process_name}[^\\\/,"]+?))),\d+,[^,]+,"?({file_path}[^"]*?)"?\s*,User"""
""",File Read,([^,]*,){3}\d+,[^,]*,\d+,[^,]+,.*/(|({file_name}[^"]*?(\.({file_ext}[^\\\/,\.\s"]+?))?))"?\s*,User"""
"""File size \(bytes\):\s*({bytes}\d+)"""
"""({operation}File Read)"""
"""({device_class}(CD-DVD|USB))"""
"""Device ID:\s*({device_id}.*)&\d+"""
]
ParserVersion = "v1.0.0"


}
```