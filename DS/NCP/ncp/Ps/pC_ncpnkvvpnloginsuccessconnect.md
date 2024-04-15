#### Parser Content
```Java
{
Name = "ncp-n-kv-vpn-login-success-connect"
Vendor = "NCP"
Product = "NCP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" connect """
""" : incoming : """
"""IP="""
]
Fields = [
"""<.+?>\w+ \d+ \d\d:\d\d:\d\d ({host}\S+)\s+connect"""
"""incoming\s*:\s*({user}[^\s@]+)(@({domain}[^\s@]+)\s*:)"""
"""IP=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""VpnEp=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""Group=({realm}\w+)"""
]
DupFields = [
"user->account"
]
ParserVersion = "v1.0.0"


}
```