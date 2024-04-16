#### Parser Content
```Java
{
Name = "delinea-centrifyztps-kv-user-switch-success-granted"
Vendor = "Delinea"
Product = "Centrify Zero Trust Privilege Services"
TimeFormat = "epoch_sec"
Conditions = [
"""Centrify Suite|dzdo"""
"""dzdo granted"""
]
Fields = [
"""utc=({time}\d{10})"""
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w.\-]+)\s"""
"""user=({user}[\w\.\-]{1,40}\$?)"""
"""\d+\|\d+\|({event_name}.+?)\|\d"""
"""status=({result}.+?)\s\w+="""
"""pid=({process_id}\d+)"""
"""service=({service_name}.+?)\s\w+="""
"""runas=({dest_user}.+?)\s\w+="""
"""EntityName =({object}.+?)\s*$"""
"""command=({process_path}({process_dir}.*?)(\/+({process_name}[^\/]+?))?)\s*(\w+=|$)"""
]
DupFields = [ "dest_user->account" ]
ParserVersion = "v1.0.0"


}
```