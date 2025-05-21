#### Parser Content
```Java
{
Name = "microsoft-evnps-kv-endpoint-login-success-6272"
Vendor = "Microsoft"
Product = "Event Viewer - NPS"
TimeFormat = "epoch_sec"
Conditions = [
"""EventIDCode=6272"""
"""Network Policy Server granted access to a user"""
]
Fields = [
"""TimeGenerated=({time}\d{10})"""
"""Message=\s*({event_name}.+?)\.\s+"""
"""EventIDCode=({event_code}\d+)"""
"""Computer=({host}[\w\-.]+)"""
"""User=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""Domain=(|({domain}[^\s]+))"""
"""User:.+?\sAccount Name:\s*(|(?:({user_type}host)/)?(({domain}[^\\\/]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|({=domain}.+?))\s*Fully Qualified Account Name:(|(({=domain}[^\\\/]+?)[\\\/]+)?({=user}.+?))"""
"""\sCalled Station Identifier:\s*(-|({dest_mac}\w{2}-\w{2}-\w{2}-\w{2}-\w{2}-\w{2})|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\sCalling Station Identifier:\s*(-|({src_mac}\w{2}-\w{2}-\w{2}-\w{2}-\w{2}-\w{2})|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\sNAS IPv(4|6) Address:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sNAS Identifier:\s*(-|({location}.+?))\s*NAS Port-Type:"""
]
ParserVersion = "v1.0.0"


}
```