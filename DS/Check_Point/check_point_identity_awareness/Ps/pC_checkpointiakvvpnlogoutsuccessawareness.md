#### Parser Content
```Java
{
Name = "checkpoint-ia-kv-vpn-logout-success-awareness"
Vendor = "Check Point"
Product = "Check Point Identity Awareness"
TimeFormat = "dMMMyyyy H:mm:ss"
Conditions = [
"""Product=Identity Awareness"""
"""logout"""
"""Source="""
"""User="""
]
Fields = [
"""src_user_group=(-|({user_group_name}[^\|]+))\|"""
"""auth_method=(-|({auth_method}[^\|]+))\|"""
"""\s+({time}\d{1,2}\w+\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2})\|"""
"""Originip=({host}[^\|]+)\|"""
"""Origin=({host}[^\|]+)\|"""
"""Action=(-|({operation}[^\|]+))\|"""
"""SIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|"""
"""SPort=({src_port}\d+)"""
"""DPort=({dest_port}\d+)"""
"""Destination=(-|({dest_host}[^\|]+))\|"""
"""DIP=(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\|"""
"""Protocol=(-|({protocol}[^\|]+))\|"""
"""IFDirection=(-|({direction}[^\|]+))\|"""
"""Reason=(-|({result_reason}[^\|]+))\|"""
"""(U|u)ser=(-|({full_name}[^\(]+)\s+\(({user}[\w\.\-]{1,40}\$?))"""
"""domain_name=(-|({domain}[^\|]+))\|"""
"""termination_reason=(-|({failure_reason}[^\|]+))\|"""
"""duration=(-|({session_duration}[^\|]+))\|"""
"""description=(-|({additional_info}[^\|]+))\|"""
]
ParserVersion = "v1.0.0"


}
```