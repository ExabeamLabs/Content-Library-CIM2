#### Parser Content
```Java
{
Name = "trapx-t-cef-alert-trigger-success-scandetected"
Vendor = "TrapX"
Product = "TrapX"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""Intelligence Event"""
"""|TrapX|"""
"""Network Scan Detected"""
]
Fields = [
"""rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s"""
"""cat=({alert_name}[^=]+?)\s\w+="""
"""src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""deviceNtDomain=({domain}[^=]{1,200})\s\w+="""
"""dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""dpt=({dest_port}\d+)\s"""
"""spt=({src_port}\d+)\s"""
"""proto=({protocol}[^=]+)\s\w+="""
"""\sexternalId=({alert_id}\d+)"""
"""CEF:([^|]*\|){6}({alert_severity}[^|]+)"""
"""CEF:([^|]*\|){5}({alert_type}[^|]+)"""
]
ParserVersion = "v1.0.0"


}
```