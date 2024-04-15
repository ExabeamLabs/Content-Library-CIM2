#### Parser Content
```Java
{
Name = "onespan-osign-kv-endpoint-login-fail-ikeyserver"
Vendor = "OneSpan"
Product = "OneSpan Sign"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
Conditions = [
"""{Input Details:"""
"""{User ID"""
"""User authentication failed"""
""" ikeyserver"""
]
Fields = [
"""\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+ikeyserver"""
"""time\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d \w+)"""
"""\{Source Location:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\{Client Location:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\{Input Details:\s*\{User ID\s*:\s*({user}[^\}]+)"""
"""\{Client Type:({login_type_text}[^\}]+)"""
"""\{Status Message\s*:\s*({event_name}[^\}]+)"""
"""({result}Failure)"""
"""\{Input Details:.+?\{Domain Name\s*:\s*({domain}[^\}]+)"""
"""\{Reason\s*:\s*({failure_reason}[^\}]+)"""
]
ParserVersion = "v1.0.0"


}
```