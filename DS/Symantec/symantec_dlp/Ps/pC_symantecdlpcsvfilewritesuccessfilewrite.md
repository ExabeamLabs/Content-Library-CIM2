#### Parser Content
```Java
{
Name = "symantec-dlp-csv-file-write-success-filewrite"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""",Rule: """
""",File Write,Begin:"""
]
Fields = [
""",(0.0.0.0|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^,]*)),([^,]*,){2}File Write,"""
""",Rule:[^\|]*\| ({operation_details}[^,]*)"""
"""Begin:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""",File Write,([^,]*,){3}\d+,"?(?: |({process_path}({process_dir}(?:[^,]+)?[\\\/])?({process_name}[^\\\/,]+?))),\d+,[^,]+,"?({file_path}.+?)"?,User""",
""",File Write,([^,]*,){3}\d+,[^,]*,\d+,[^,]+,.*/({file_name}.+?(\.({file_ext}[^\.,\s"]+))?)"?,User"""
"""User\s*(Name)?:\s+((?i)SYSTEM|None|NETWORK|LOCAL|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),Domain"""
"""({operation}File Write)"""
"""Domain\s*(Name)?:\s+((?i)NT AUTHORITY|None|({domain}.+?)),Action Type"""
"""File size \(bytes\):\s+({bytes}\d+)"""
"""Device ID:\s+({device_id}.*)&\d+"""
"""({device_class}(CD-DVD|USB))"""
"""SymantecServer:\s*({client}[^,]+?)\s*(,|$)"""
"""Rule:\s+(?:|({rule}[^,]+)),""",
]
ParserVersion = "v1.0.0"


}
```