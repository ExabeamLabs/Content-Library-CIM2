#### Parser Content
```Java
{
Name = "microsoft-evprintservice-kv-printer-activity-success-307"
Vendor = "Microsoft"
Product = "Event Viewer - PrintService"
TimeFormat = "epoch_sec"
Conditions = [
"""Source=Microsoft-Windows-PrintService"""
"""EventID=307"""
""" owned by """
""" was printed on """
]
Fields = [
"""TimeGenerated=({time}\d{10})"""
"""Computer=({host}[\w\-.]+)"""
"""User=({user}[^\s]+)"""
"""Domain=({domain}[^\s]+)"""
"""EventID=({event_code}\d+)"""
"""Opcode=({action}.+?)\s*(\w+=|$)"""
"""Message=({activity_1}.*?\s*(?i)Document) \d+,"""
"""Message=.+?owned by [^\s]+\s*.*?( on [^\s]+)?({activity_2}.+?) on ({printer_name}.+?)(\.\s+|\s+through)"""
"""Message=[^,]+,\s+({object}.+?) owned by"""
"""Message=.+?owned by.+? on \\*(?:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?)) was """
"""Message=.+?through port (\w+_)?(?:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|\\*({dest_host}.+?))\.\s+"""
"""Message=.+?Size in bytes:\s*({bytes}\d+)"""
"""Message=.+?Pages printed:\s*({num_pages}\d+)"""
]
ParserVersion = "v1.0.0"


}
```