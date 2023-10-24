#### Parser Content
```Java
{
Name = "microsoft-evprintservice-kv-printer-activity-success-document"
Vendor = "Microsoft"
Product = "Event Viewer - PrintService"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""Microsoft-Windows-PrintService"""
"""Printing a document"""
]
Fields = [
"""({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
"""ComputerName =({host}[^\s]+)"""
"""Sid=({user_sid}[^\s]+)"""
"""OpCode=({result}.+?)\s+\w+="""
"""EventCode=({event_code}\d+)"""
"""Message=({activity_1}.*?\s*(?i)Document) \d+,"""
"""owned by [^\s]+\s*.*?( on [^\s]+)?({activity_2}.+?) on ({printer_name}.+?)(\.\s+|\s+through)"""
"""Message=[^,]+,\s+({object}.+?) owned by"""
"""owned by ({user}[\w\.\-]{1,40}\$?) """,
"""owned by.+? on \\*(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?)) was """
"""through port (\w+_)?(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|\\*({dest_host}[\w\-.]+?))\.\s+"""
"""Size in bytes:\s+({bytes}\d+)"""
"""Pages printed:\s+({num_pages}\d{1,9})\D"""
"""[\[\(]+({access}Read-Only)[\]\)]+"""
"""TaskCategory=({operation}[^=]+?)\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```