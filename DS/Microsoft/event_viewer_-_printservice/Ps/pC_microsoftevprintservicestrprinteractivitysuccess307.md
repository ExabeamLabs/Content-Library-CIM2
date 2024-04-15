#### Parser Content
```Java
{
Name = "microsoft-evprintservice-str-printer-activity-success-307"
Vendor = "Microsoft"
Product = "Event Viewer - PrintService"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""Microsoft-Windows-PrintService"""
"""Printing a document"""
"""rn="""
]
Fields = [
"""owned by [^\s]+\s*.*?( on [^\s]+)?({activity_2}.+?) on ({printer_name}.+?)(\.\s+|\s+through)"""
"""owned by ({user}.+?) (to|on) """
"""owned by.+? on \\*(?:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?)) was """
"""through port (\w+_)?(?:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|\\*({dest_host}.+?))\.\s+"""
"""Size in bytes:\s+({bytes}\d+)"""
"""Pages printed:\s+({num_pages}\d+)"""
"""[\[\(]+({access}Read-Only)[\]\)]+"""
"""({event_code}307)"""
"""Document \d+,\s+({object}.+?)\s*owned by"""
"""\s({time}\w+\s+\d\d\s+\d\d:\d\d:\d\d\s+\d\d\d\d),"""
"""PrintService,({user_sid}\w+-\w+-\w+-\w+-\w+-\w+-\w+-\w+),"""
""",({host}[^,]+),Printing a document"""
"""({event_name}Printing a document)"""
]
DupFields = [
"event_name->operation"
]
ParserVersion = "v1.0.0"


}
```