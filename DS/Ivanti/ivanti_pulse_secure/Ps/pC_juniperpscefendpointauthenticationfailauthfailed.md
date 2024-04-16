#### Parser Content
```Java
{
Name = "juniper-ps-cef-endpoint-authentication-fail-authfailed"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Juniper|"""
"""|Primary authentication failed|"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""({failure_reason}(Primary|Secondary) authentication failed) for\s+(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)(\/({realm}.+?))\s+from=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsuser=(System|({user}[\w\.\-]{1,40}\$?))"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```