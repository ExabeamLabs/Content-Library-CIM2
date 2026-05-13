#### Parser Content
```Java
{
Name = "delinea-centrifyztps-kv-endpoint-logout-sshdconnectionclose"
Vendor = "Delinea"
Product = "Centrify Zero Trust Privilege Services"
TimeFormat = "epoch_sec"
Conditions = [
"""Centrify Suite|Centrify sshd"""
"""SSHD connection close"""
]
Fields = [
"""utc=({time}\d{10})"""
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w.\-]+)\s"""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\d+\|\d+\|({event_name}.+?)\|\d"""
"""status=({result}.+?)\s\w+="""
"""pid=({process_id}\d+)"""
"""service=({service_name}.+?)\s\w+="""
"""runas=({account}({dest_user}.+?))\s\w+="""
"""EntityName =({object}.+?)\s*$"""
"""authMechanism=({auth_method}.+?)\s\w+="""
"""reason=({result_reason}.+?)$"""
"""client=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""centrifyEventID=({event_code}\d+)"""
]
ParserVersion = "v1.0.0"


}
```