#### Parser Content
```Java
{
Name = "rsa-netwitness-cef-app-login-success-authsuccess"
Product = "RSA NetWitness Platform"
Vendor = "RSA"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""CEF:"""
"""RSA|NetWitness Audit"""
"""|AUTHENTICATION|login|"""
"""outcome=success"""
]
Fields = [
"""rt=({time}\w+ \d+ \d+ \d+:\d+:\d+)"""
"""src=(127.0.0.1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""spt=({src_port}\d+)"""
"""sessionId=({session_id}\d+)"""
"""({app}NetWitness)"""
"""\Wsuser=((?i)system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s\w+=|\()"""
"""sourceServiceName =({service_name}[^=]+?)\s\w+="""
"""outcome=({result}[^=]+?)\s\w+="""
"""userRole=({role}[^=]+?)\s*(\w+=|$)"""
"""CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```