#### Parser Content
```Java
{
Name = "symantec-dlp-csv-file-write-success-filedelete"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""",Rule: """
""",File Delete,Begin:"""
]
Fields = [
""",(0.0.0.0|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^,]*)),([^,]*,){2}File Delete,"""
""",Rule:[^\|]*\| ({operation_details}[^,]*)"""
"""Begin:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""",File Delete,([^,]*,){3}\d+,"?(?: |({process_path}({process_dir}(?:[^,]+)?[\\\/])?({process_name}[^\\\/,]+?))),\d+,[^,]+,"?({file_path}.+?)"?,User""",
""",File Delete,([^,]*,){3}\d+,[^,]*,\d+,[^,]+,.*/({file_name}.+?)"?,User"""
"""User:\s+({user}.+?),Domain"""
"""({operation}File Delete)"""
"""Domain:\s+({domain}.+?),Action Type"""
"""File size \(bytes\):\s+({bytes}\d+)"""
"""Device ID:\s+({device_id}.*)&\d+"""
"""({device_type}(CD-DVD|USB))"""
]
ParserVersion = "v1.0.0"


}
```