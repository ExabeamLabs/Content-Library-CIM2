#### Parser Content
```Java
{
Name = "checkpoint-sg-kv-vpn-login-fail-connectra"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = "ddMMMyyyy HH:mm:ss"
Conditions = [
"""|product=Connectra|"""
"""|event_type=Login|"""
"""|status=Failure|"""
]
Fields = [
"""\|(U|u)ser=({first_name}[^,@\|]+),\s*({last_name}[^@\|]+)@({domain}[^\s\|]+)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)\s*(\||$)"""
"""\|user_dn=({user_ou}[^\|]+)\|"""
"""\|user_group=({realm}[^\|]+)"""
"""\|time=({time}\d+\w+\d\d\d\d \d+:\d+:\d+)"""
"""\|src=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w.\-]+))\|"""
"""\|office_mode_ip=({host}[a-fA-F\d.:]+)"""
"""\|Hostname=({host}[^\|]+)\|"""
"""\|reason=({failure_reason}[^\|]+)\|"""
]
ParserVersion = "v1.0.0"


}
```