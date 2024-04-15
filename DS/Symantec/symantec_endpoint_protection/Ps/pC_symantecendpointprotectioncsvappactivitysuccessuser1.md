#### Parser Content
```Java
{
Name = "symantec-endpointprotection-csv-app-activity-success-user1"
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Scan ID:"""
"""End Time:"""
"""Computer:"""
"""Domain Name:"""
"""User1:"""
]
Fields = [
"""({time}\d+-\d+-\d+ \d+:\d+:\d+)"""
"""Scan ID:\s*({scan_id}\d+)"""
"""Computer:\s*({host}[^,]+)"""
"""IP Address:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Server Name:\s*({dest_host}[^.\s,]+)"""
"""User1:\s*(SYSTEM|({user}[^,]+))"""
"""Group Name:\s({group_name}[^,]+)"""
"""Domain Name:\s*({domain}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```