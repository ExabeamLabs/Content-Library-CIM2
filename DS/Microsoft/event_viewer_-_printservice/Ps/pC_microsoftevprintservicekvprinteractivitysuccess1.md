#### Parser Content
```Java
{
Name = "microsoft-evprintservice-kv-printer-activity-success-1"
Vendor = "Microsoft"
Product = "Event Viewer - PrintService"
TimeFormat = "epoch_sec"
Conditions = [
"""Source=Print"""
"""EventIDCode=1"""
]
Fields = [
"""\sTimeGenerated=({time}\d{10})"""
"""\sComputer=({host}\S+)"""
"""\sUser=({user}.+?)\s+\w+="""
"""\sDomain=({domain}.+?)\s+\w+="""
"""\sEventIDCode=({event_code}\d+)"""
"""Message=({activity_1}.*?\s*(?i)Document) \d+,"""
"""owned by [^\s]+\s*.*?( on [^\s]+)?({activity_2}.+?) on ({printer_name}.+?)(\.\s+|\s+through)"""
"""Message=[^,]+,\s+({object}.+?) owned by"""
"""owned by ({user}.+?) (to|on|was) """
"""owned by.+? on \\*(?:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?)) was """
"""through port (\w+_)?(?:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?[_\w]*|\\*({dest_host}.+?))\.\s+"""
"""Size in bytes:\s+({bytes}\d+)"""
"""Pages printed:\s+({num_pages}\d+)"""
]
ParserVersion = "v1.0.0"


}
```