#### Parser Content
```Java
{
Name = "microsoft-evprintservice-str-printer-activity-success-printed"
Vendor = "Microsoft"
Product = "Event Viewer - PrintService"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Microsoft-Windows-PrintService["""
""" owned by """
""" was printed on """
]
Fields = [
"""({host}\S+)\sMicrosoft-Windows-PrintService\["""
"""Microsoft-Windows-PrintService\[[^:]+:\s((NT AUTHORITY\\)|({domain}[^\\]+)\\)?((SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)):"""
"""EventID ({event_code}\d+)"""
"""\]:\s*({time}\d{4}\-\d\d\-\d\d \d\d:\d\d:\d\d)\s({host}[^\s]+)\s[^\s]+\s({event_code}\d+)\s(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s"""
"""\s({activity_1}Document) \d+,"""
"""owned by [^\s]+\s*[^$]*?( on [^\s]+)?({activity_2}[^\s]+?) on ({printer_name}[^$]+?)(\.\s+|\s+through)"""
"""\sDocument \d+,\s+({object}[^$"]+?)\s+owned by"""
"""owned by.+? on \\*(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}\S+)) was """
"""through port (\w+_)?(?:nul|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|\\*({dest_host}[\w\-.]+?))(_\d+)?:?\.\s+Size in bytes"""
"""Size in bytes:\s*({bytes}\d+)"""
"""Pages printed:\s*({num_pages}\d+)"""
]
ParserVersion = "v1.0.0"


}
```