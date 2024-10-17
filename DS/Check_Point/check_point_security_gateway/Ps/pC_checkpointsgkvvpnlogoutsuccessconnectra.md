#### Parser Content
```Java
{
Name = "checkpoint-sg-kv-vpn-logout-success-connectra"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = ["ddMMMyyyy HH:mm:ss","ddMMMyyyy  H:mm:ss"]
Conditions = [
""",cvpn_category=Session,"""
""",product=Connectra,"""
""",event_type=Logout,"""
]
Fields = [
"""\,(U|u)ser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\,user_dn=({user_ou}[^\,]+)"""
"""\s+time=({time}\d+\w+\s+\d+:\d+:\d+)"""
"""\,src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\,reason=({result_reason}[^\,]+)"""
]
ParserVersion = "v1.0.0"


}
```